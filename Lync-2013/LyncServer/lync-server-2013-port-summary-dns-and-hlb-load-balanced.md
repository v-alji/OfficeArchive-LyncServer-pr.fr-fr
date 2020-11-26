---
title: 'Lync Server 2013 : Résumé des ports - Équilibrage de charge DNS et matérielle'
description: 'Lync Server 2013 : Summary Summary-DNS et HLB Load Balanced.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424337"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="46b4e-103">Résumé des ports - Équilibrage de charge DNS et matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46b4e-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46b4e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46b4e-104">

<span> </span></span></span>

<span data-ttu-id="46b4e-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="46b4e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="46b4e-106">La configuration requise pour les ports de pare-feu pour un seul directeur consiste à utiliser les ports utilisés pour établir une communication avec le directeur à partir de l’interface interne ou du réseau interne du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="46b4e-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="46b4e-107">Microsoft Lync Server 2013 par défaut s’attend à ce que les ports HTTP/TCP 8080 et HTTPs/TCP 4443 soient ouverts du proxy inverse au directeur, ainsi qu’au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="46b4e-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="46b4e-108">Par ailleurs, il doit y avoir une communication SIP (Session Initiation Protocol) à partir de l’interface interne du serveur Edge au directeur et au serveur principal et au pool frontal.</span><span class="sxs-lookup"><span data-stu-id="46b4e-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="46b4e-109">Le protocole SIP utilise SIP/MTLS/TCP 5061 du serveur Edge au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="46b4e-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="46b4e-110">Une règle qui autorise la communication SIP/MTLS/TCP 5061 à partir du réalisateur, du pool frontal et du serveur frontal vers l’interface interne du serveur Edge doit également être créée.</span><span class="sxs-lookup"><span data-stu-id="46b4e-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="46b4e-111">Ports et protocoles de Director uniques pour les définitions de pare-feu</span><span class="sxs-lookup"><span data-stu-id="46b4e-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46b4e-112">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="46b4e-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="46b4e-113">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="46b4e-113">Source IP address</span></span></th>
<th><span data-ttu-id="46b4e-114">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="46b4e-114">Destination IP address</span></span></th>
<th><span data-ttu-id="46b4e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="46b4e-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46b4e-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="46b4e-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="46b4e-117">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="46b4e-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="46b4e-118">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="46b4e-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="46b4e-119">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée aux services d’adresse IP du directeur HLB et aux services Web du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="46b4e-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46b4e-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="46b4e-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="46b4e-121">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="46b4e-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="46b4e-122">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="46b4e-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="46b4e-123">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée aux services d’adresse IP du directeur HLB et aux services Web du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="46b4e-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46b4e-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="46b4e-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="46b4e-125">directeur</span><span class="sxs-lookup"><span data-stu-id="46b4e-125">Director</span></span></p></td>
<td><p><span data-ttu-id="46b4e-126">Pool frontal ou serveur frontal</span><span class="sxs-lookup"><span data-stu-id="46b4e-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="46b4e-127">Communications entre les serveurs entre le directeur HLB VIP et le serveur frontal ou les serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="46b4e-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46b4e-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="46b4e-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="46b4e-129">Clients internes</span><span class="sxs-lookup"><span data-stu-id="46b4e-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="46b4e-130">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="46b4e-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="46b4e-131">Le directeur fournit des services Web aux clients externes et internes.</span><span class="sxs-lookup"><span data-stu-id="46b4e-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46b4e-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="46b4e-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="46b4e-133">Clients internes</span><span class="sxs-lookup"><span data-stu-id="46b4e-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="46b4e-134">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="46b4e-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="46b4e-135">Le directeur fournit des services Web aux clients externes et internes.</span><span class="sxs-lookup"><span data-stu-id="46b4e-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46b4e-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="46b4e-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="46b4e-137">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="46b4e-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="46b4e-138">directeur</span><span class="sxs-lookup"><span data-stu-id="46b4e-138">Director</span></span></p></td>
<td><p><span data-ttu-id="46b4e-139">Communication SIP du serveur Edge au directeur ainsi qu’aux serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="46b4e-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46b4e-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="46b4e-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="46b4e-141">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46b4e-141">Any</span></span></p></td>
<td><p><span data-ttu-id="46b4e-142">directeur</span><span class="sxs-lookup"><span data-stu-id="46b4e-142">Director</span></span></p></td>
<td><p><span data-ttu-id="46b4e-143">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="46b4e-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46b4e-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="46b4e-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="46b4e-145">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46b4e-145">Any</span></span></p></td>
<td><p><span data-ttu-id="46b4e-146">directeur</span><span class="sxs-lookup"><span data-stu-id="46b4e-146">Director</span></span></p></td>
<td><p><span data-ttu-id="46b4e-147">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="46b4e-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46b4e-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="46b4e-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="46b4e-149">Indifférente</span><span class="sxs-lookup"><span data-stu-id="46b4e-149">Any</span></span></p></td>
<td><p><span data-ttu-id="46b4e-150">directeur</span><span class="sxs-lookup"><span data-stu-id="46b4e-150">Director</span></span></p></td>
<td><p><span data-ttu-id="46b4e-151">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="46b4e-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="46b4e-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46b4e-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

