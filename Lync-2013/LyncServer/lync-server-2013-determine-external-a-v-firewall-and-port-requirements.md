---
title: 'Lync Server 2013 : Définition de la configuration requise pour le pare-feu A/V et les ports'
description: 'Lync Server 2013 : déterminer les exigences de port et de pare-feu A/V externes'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine external A/V firewall and port requirements
ms:assetid: 3b849dc7-175d-40d1-820d-80e6ade6d332
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425882(v=OCS.15)
ms:contentKeyID: 48183872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 38c2a8c1e8e332a4a1e65adb87a1e962e82941c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429511"
---
# <a name="determine-external-av-firewall-and-port-requirements-for-lync-server-2013"></a><span data-ttu-id="b6d47-103">Définition de la configuration requise pour le pare-feu A/V et les ports pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6d47-103">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6d47-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6d47-104">

<span> </span></span></span>

<span data-ttu-id="b6d47-105">_**Dernière modification de la rubrique :** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="b6d47-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="b6d47-106">Les communications audio/vidéo (A/V) peuvent être complexes.</span><span class="sxs-lookup"><span data-stu-id="b6d47-106">Audio/Video (A/V) communication can be a complex.</span></span> <span data-ttu-id="b6d47-107">En raison de la nature des protocoles utilisés dans A/V et de la manière dont les clients et les serveurs utilisent les protocoles, une section spéciale est garante d’expliquer les différences entre les versions client et serveur.</span><span class="sxs-lookup"><span data-stu-id="b6d47-107">Because of the nature of protocols used in A/V and how clients and servers use the protocols, a special section is warranted to explain the differences between client and server versions.</span></span>

<span data-ttu-id="b6d47-108">Utilisez le pare-feu A/V et la table de port suivants pour déterminer les exigences de pare-feu et les ports à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b6d47-108">Use the following A/V Firewall and Port table to determine firewall requirements and which ports to open.</span></span> <span data-ttu-id="b6d47-109">Ensuite, examinez la terminologie de la traduction d’adresses réseau (NAT), car la traduction d’adresses réseau peut être implémentée de diverses manières.</span><span class="sxs-lookup"><span data-stu-id="b6d47-109">Then, review the network address translation (NAT) terminology because NAT can be implemented in many different ways.</span></span> <span data-ttu-id="b6d47-110">Pour obtenir un exemple détaillé de paramètres de port de pare-feu, consultez les architectures de référence dans les [scénarios pour l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="b6d47-110">For a detailed example of firewall port settings, see the reference architectures in [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

### <a name="general-protocol-usage-for-udp-and-tcp-in-audiovideo-and-media-traffic"></a><span data-ttu-id="b6d47-111">Utilisation générale des protocoles pour UDP et TCP dans le trafic audio/vidéo et multimédia</span><span class="sxs-lookup"><span data-stu-id="b6d47-111">General Protocol Usage for UDP and TCP in Audio/Video and Media Traffic</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6d47-112">Transport audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="b6d47-112">Audio/Video Transport</span></span></th>
<th><span data-ttu-id="b6d47-113">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b6d47-113">Usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6d47-114">UDP</span><span class="sxs-lookup"><span data-stu-id="b6d47-114">UDP</span></span></p></td>
<td><p><span data-ttu-id="b6d47-115">Protocole préféré de couche de transport pour le son et la vidéo</span><span class="sxs-lookup"><span data-stu-id="b6d47-115">Preferred transport layer protocol for audio and video</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6d47-116">TCP</span><span class="sxs-lookup"><span data-stu-id="b6d47-116">TCP</span></span></p></td>
<td><p><span data-ttu-id="b6d47-117">Protocole de couche de transport de secours pour le son et la vidéo</span><span class="sxs-lookup"><span data-stu-id="b6d47-117">Fallback transport layer protocol for audio and video</span></span></p>
<p><span data-ttu-id="b6d47-118">Protocole requis pour le partage d’application sur Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6d47-118">Required transport layer protocol for application sharing to Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013</span></span></p>
<p><span data-ttu-id="b6d47-119">Protocole requis pour le transfert de fichiers vers Lync Server 2010 et Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6d47-119">Required transport layer protocol for file transfer to Lync Server 2010 and Lync Server 2013</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="external-av-firewall-port-requirements-for-external-user-access"></a><span data-ttu-id="b6d47-120">Exigences relatives aux ports de pare-feu A/V externes pour l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="b6d47-120">External A/V Firewall Port Requirements for External User Access</span></span>

<span data-ttu-id="b6d47-121">La configuration requise pour les ports de pare-feu pour les interfaces SIP et de conférence externes (et internes) est cohérente, quelle que soit la version de votre client ou la version du partenaire de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b6d47-121">The firewall port requirements for external (and internal) SIP and conferencing interfaces are consistent, regardless of the version of your client or the version of the federation partner.</span></span>

<span data-ttu-id="b6d47-122">Le même type n’est pas vrai pour l’interface externe du périphérique audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6d47-122">The same is not true for the Audio/Video Edge external interface.</span></span> <span data-ttu-id="b6d47-123">Dans le cadre de la Fédération avec Office Communications Server 2007, le service Edge A/V exige que les règles de pare-feu externe autorisent le trafic RTP/TCP et RTP/UDP dans les 50 000 à 59 999 par le biais de la plage de port.</span><span class="sxs-lookup"><span data-stu-id="b6d47-123">For federation with Office Communications Server 2007, the A/V Edge service requires that external firewall rules allow RTP/TCP and RTP/UDP traffic in the 50,000 through 59,999 port range to flow in both directions.</span></span> <span data-ttu-id="b6d47-124">Le tableau précédent part du principe que Lync Server 2013 est le principal partenaire de Fédération et qu’il est configuré pour communiquer avec l’un des autres types de partenaires de Fédération répertoriés.</span><span class="sxs-lookup"><span data-stu-id="b6d47-124">The previous table assumes that Lync Server 2013 is the primary federation partner and it is being configured to communicate with one of the other federation partner types listed.</span></span>

<span data-ttu-id="b6d47-125">La configuration de la plage de ports audio/vidéo de 50000-59,999 doit prendre en compte que la plage de port va contenir les ports sources pour les communications avec les partenaires de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b6d47-125">Configuring the Audio/Video port range of 50,000-59,999 must take into account that the port range will contain the source ports for communications to federation partners.</span></span> <span data-ttu-id="b6d47-126">En détail, considérez qu’une communication est lancée à partir d’un partenaire de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b6d47-126">In detail, consider that a communication is initiated from a federation partner.</span></span> <span data-ttu-id="b6d47-127">La communication des ports de service Edge A/V dans la plage 50000-59,999 se connectera au port TCP 443 du service Edge A/V du partenaire.</span><span class="sxs-lookup"><span data-stu-id="b6d47-127">The communication from the A/V Edge service ports in the 50,000-59,999 range will connect to the expected port TCP 443 of the partner’s A/V Edge service.</span></span> <span data-ttu-id="b6d47-128">À l’inverse, le trafic entrant vers votre service de port TCP 443 a un port source dans la plage comprise entre 50000 et 59,999.</span><span class="sxs-lookup"><span data-stu-id="b6d47-128">Conversely, inbound traffic to your A/V Edge service port TCP 443 will have a source port in the range of 50,000-59,999.</span></span>

<span data-ttu-id="b6d47-129">Les pare-feu et les stratégies différents pour l’administration du pare-feu peuvent nécessiter la configuration de règles de destination uniquement, ou exiger la configuration de la source et de la destination.</span><span class="sxs-lookup"><span data-stu-id="b6d47-129">Different firewalls and policies for firewall administration may require only destination rules to be configured, or they may require both source and destination to be configured.</span></span> <span data-ttu-id="b6d47-130">S’il s’agit de la configuration requise pour les ports de destination uniquement, les exigences audio et vidéo sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6d47-130">If your requirements are for destination ports only, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6d47-131">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="b6d47-131">Source IP</span></span></th>
<th><span data-ttu-id="b6d47-132">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="b6d47-132">Destination IP</span></span></th>
<th><span data-ttu-id="b6d47-133">Port de destination</span><span class="sxs-lookup"><span data-stu-id="b6d47-133">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6d47-134">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-134">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-135">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-135">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-136">TCP 443</span><span class="sxs-lookup"><span data-stu-id="b6d47-136">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6d47-137">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-137">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-138">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-138">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-139">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="b6d47-139">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6d47-140">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-140">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-141">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-141">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-142">TCP 443</span><span class="sxs-lookup"><span data-stu-id="b6d47-142">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6d47-143">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-143">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-144">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-144">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-145">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="b6d47-145">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6d47-146">Si vos stratégies nécessitent à la fois les définitions des règles de pare-feu entrant et sortant, les exigences audio et vidéo sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6d47-146">If your policies require both inbound and outbound firewall rule definitions, the Audio/Video requirements are:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b6d47-147">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="b6d47-147">Source IP</span></span></th>
<th><span data-ttu-id="b6d47-148">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="b6d47-148">Destination IP</span></span></th>
<th><span data-ttu-id="b6d47-149">Port source</span><span class="sxs-lookup"><span data-stu-id="b6d47-149">Source Port</span></span></th>
<th><span data-ttu-id="b6d47-150">Port de destination</span><span class="sxs-lookup"><span data-stu-id="b6d47-150">Destination Port</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6d47-151">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-151">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-152">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-152">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-153">TCP 50 000 à 59 999</span><span class="sxs-lookup"><span data-stu-id="b6d47-153">TCP 50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="b6d47-154">TCP 443</span><span class="sxs-lookup"><span data-stu-id="b6d47-154">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6d47-155">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-155">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-156">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-156">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-157">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="b6d47-157">UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="b6d47-158">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="b6d47-158">UDP 3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6d47-159">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-159">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-160">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-160">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-161">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-161">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-162">TCP 443</span><span class="sxs-lookup"><span data-stu-id="b6d47-162">TCP 443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6d47-163">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-163">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-164">Interface de service Edge A/V</span><span class="sxs-lookup"><span data-stu-id="b6d47-164">A/V Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="b6d47-165">Indifférente</span><span class="sxs-lookup"><span data-stu-id="b6d47-165">Any</span></span></p></td>
<td><p><span data-ttu-id="b6d47-166">UDP 3478</span><span class="sxs-lookup"><span data-stu-id="b6d47-166">UDP 3478</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="b6d47-167">La configuration de Microsoft Office Communications Server 2007 nécessite une configuration légèrement différente.</span><span class="sxs-lookup"><span data-stu-id="b6d47-167">Microsoft Office Communications Server 2007 requires a slightly different configuration.</span></span> <span data-ttu-id="b6d47-168">Les plages de port TCP et UDP de 50000-59,999 doivent être ouvertes en entrée et en sortie.</span><span class="sxs-lookup"><span data-stu-id="b6d47-168">The TCP and UDP port range of 50,000-59,999 must be open inbound and outbound.</span></span> <span data-ttu-id="b6d47-169">Cette condition est uniquement requise pour Office Communicator 2007.</span><span class="sxs-lookup"><span data-stu-id="b6d47-169">This requirement is only for Office Communicator 2007.</span></span> <span data-ttu-id="b6d47-170">Office Communications Server 2007 R2, Lync Server 2010 et Lync Server 2013 nécessitent uniquement la plage TCP 50000-59,999 ouverte.</span><span class="sxs-lookup"><span data-stu-id="b6d47-170">Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013 only require TCP range 50,000-59,999 open outbound.</span></span>



</div>

</div>

<div>

## <a name="nat-requirements-for-the-edge-service"></a><span data-ttu-id="b6d47-171">Configuration NAT requise pour le service Edge</span><span class="sxs-lookup"><span data-stu-id="b6d47-171">NAT requirements for the Edge service</span></span>

<span data-ttu-id="b6d47-172">Les exigences suivantes concernant tar s’appliquent si vous choisissez de configurer des adresses IP privées non routables pour le service Edge :</span><span class="sxs-lookup"><span data-stu-id="b6d47-172">The following NAT requirements apply if you choose to configure non-routable private IP addresses for the Edge service:</span></span>

  - <span data-ttu-id="b6d47-173">TAR ne peut être utilisée qu’avec l’équilibrage de charge DNS.</span><span class="sxs-lookup"><span data-stu-id="b6d47-173">NAT can only be used with DNS load-balancing.</span></span> <span data-ttu-id="b6d47-174">TAR n’est pas pris en charge avec une topologie de bord de l’équilibrage de charge matérielle (HLB).</span><span class="sxs-lookup"><span data-stu-id="b6d47-174">NAT is not supported with a hardware load balancing (HLB) Edge topology.</span></span>

  - <span data-ttu-id="b6d47-175">TAR ne peut être utilisée que sur l’interface latérale externe.</span><span class="sxs-lookup"><span data-stu-id="b6d47-175">NAT can only be used on the external Edge interface.</span></span> <span data-ttu-id="b6d47-176">TAR n’est pas pris en charge sur l’interface latérale interne.</span><span class="sxs-lookup"><span data-stu-id="b6d47-176">NAT is not supported on the internal Edge interface.</span></span>

  - <span data-ttu-id="b6d47-177">TAR doit être symétrique pour le trafic entrant et sortant.</span><span class="sxs-lookup"><span data-stu-id="b6d47-177">NAT must be symmetric for incoming and outgoing traffic.</span></span>
    
  - <span data-ttu-id="b6d47-178">Pour le trafic provenant d’Internet, tar doit remplacer l’adresse IP de destination par l’adresse IP publique compatible NAT du service Edge A/V par son adresse IP externe.</span><span class="sxs-lookup"><span data-stu-id="b6d47-178">For traffic from the Internet, NAT must change the destination IP address from the NAT-enabled public IP address of the A/V Edge service to its external IP address.</span></span> <span data-ttu-id="b6d47-179">L’adresse IP source doit rester intacte, de sorte que le service Edge A/V peut trouver le chemin multimédia optimal.</span><span class="sxs-lookup"><span data-stu-id="b6d47-179">The source IP address must remain intact, so that the A/V Edge service can find the optimal media path.</span></span>
  
  <span data-ttu-id="b6d47-180">Par exemple, dans la direction entrante dans l’illustration ci-dessous, l’adresse IP publique 131.107.155.30 a été remplacée par l’adresse IP (privée) 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="b6d47-180">For example, in the inbound direction in the figure below, the public IP address 131.107.155.30 was changed to the external (private) IP address 10.45.16.10.</span></span> <span data-ttu-id="b6d47-181">L’adresse IP source reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="b6d47-181">The source IP address remained unchanged.</span></span>
  
  - <span data-ttu-id="b6d47-182">Pour le trafic du service Edge A/V vers Internet, tar doit remplacer l’adresse IP source par l’adresse IP externe du service Edge A/V par l’adresse IP publique compatible NAT.</span><span class="sxs-lookup"><span data-stu-id="b6d47-182">For traffic from the A/V Edge service to the Internet, NAT must change the source IP address from the external IP address of the A/V Edge service to the NAT-enabled public IP address.</span></span>

<span data-ttu-id="b6d47-183">Par exemple, dans la direction sortante dans la figure ci-dessous, l’adresse IP (privée) 10.45.16.10 a été remplacée par l’adresse IP publique 131.107.155.30.</span><span class="sxs-lookup"><span data-stu-id="b6d47-183">For example, in the outbound direction in the figure below, the external (private) IP address 10.45.16.10 was changed to the public IP address 131.107.155.30.</span></span>

<span data-ttu-id="b6d47-184">**La figure ci-dessous montre comment tar modifie l’adresse IP de destination pour le trafic entrant et l’adresse IP source pour le trafic sortant.**</span><span class="sxs-lookup"><span data-stu-id="b6d47-184">**The figure below shows how NAT changes the destination IP address for inbound traffic and the source IP Address for outbound traffic.**</span></span>

<span data-ttu-id="b6d47-185">![Modification des adresses IP de destination/source](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Modification des adresses IP de destination/source")</span><span class="sxs-lookup"><span data-stu-id="b6d47-185">![Changing destination/source IP addresses](images/Gg425882.0fee7ec5-4cb8-4aff-9164-e7fbab73336d(OCS.15).jpg "Changing destination/source IP addresses")</span></span>

<span data-ttu-id="b6d47-186">Les points clés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b6d47-186">The key points are:</span></span>

  - <span data-ttu-id="b6d47-187">Le trafic entrant sur le serveur exécutant le service Edge A/V, l’adresse IP source reste inchangée mais l’adresse IP de destination passe d' 131.107.155.30 à l’adresse IP traduite de 10.45.16.10.</span><span class="sxs-lookup"><span data-stu-id="b6d47-187">Traffic that is inbound to the server running the A/V Edge service, the source IP address does not change but the destination IP address changes from 131.107.155.30 to the translated IP address of 10.45.16.10.</span></span>

  - <span data-ttu-id="b6d47-188">Le trafic sortant du serveur exécutant le service Edge A/V vers la station de travail, l’adresse IP source passe de l’adresse IP publique du serveur à l’adresse IP publique du serveur exécutant le service Edge A/V.</span><span class="sxs-lookup"><span data-stu-id="b6d47-188">Traffic that is outbound from the server running the A/V Edge service back to the workstation, the source IP address changes from the server’s public IP address to the public IP address of the server running the A/V Edge service.</span></span> <span data-ttu-id="b6d47-189">L’adresse IP de destination reste l’adresse IP publique de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="b6d47-189">The destination IP remains the workstation’s public IP address.</span></span> <span data-ttu-id="b6d47-190">Une fois que le paquet A quitté le premier périphérique NAT en sortie, la règle sur le périphérique NAT change l’adresse IP source du serveur exécutant l’adresse IP de l’interface externe A/V (10.45.16.10) sur son adresse IP publique (131.107.155.30).</span><span class="sxs-lookup"><span data-stu-id="b6d47-190">After the packet leaves the first NAT device outbound, the rule on the NAT device changes the source IP address of the server running the A/V Edge service external interface IP address (10.45.16.10) to its public IP address (131.107.155.30).</span></span>

<span data-ttu-id="b6d47-191"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6d47-191"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

