---
title: 'Lync Server 2013 : Résumé des ports - Pool directeur mis à l’échelle, équilibreur de charge matérielle'
description: 'Lync Server 2013 : liste de répertoires de synthèse à l’échelle de ports, équilibrage de charge matérielle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled Director pool, hardware load balancer
ms:assetid: 6ae2f4ac-5b64-4e45-8253-133308f5812d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204983(v=OCS.15)
ms:contentKeyID: 48184434
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10bfb3a3ad3a38b6cb0e46414bf22deecc71d7b5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442795"
---
# <a name="port-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="0c4bd-103">Résumé des ports - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c4bd-103">Port summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c4bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c4bd-104">

<span> </span></span></span>

<span data-ttu-id="0c4bd-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="0c4bd-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="0c4bd-106">La configuration requise pour les ports de pare-feu pour un pool de directeurs est composée des ports utilisés pour établir une communication avec le directeur à partir de l’interface interne du serveur Edge ou de l’interface interne du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-106">Firewall port requirements for a Director pool consist of the ports that are used to establish communication with the Director from the internal interface of the Edge Server or internal-facing interface of the reverse proxy.</span></span> <span data-ttu-id="0c4bd-107">Microsoft Lync Server 2013 par défaut s’attend à ce que les ports HTTP/TCP 8080 et HTTPs/TCP 4443 soient ouverts du proxy inverse au directeur, ainsi qu’au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="0c4bd-108">Par ailleurs, il doit y avoir une communication SIP (Session Initiation Protocol) à partir de l’interface interne du serveur Edge au directeur et au serveur principal et au pool frontal.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="0c4bd-109">Le protocole SIP utilise SIP/MTLS/TCP 5061 du serveur Edge au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="0c4bd-110">Une règle qui autorise la communication SIP/MTLS/TCP 5061 à partir du réalisateur, du pool frontal et du serveur frontal vers l’interface interne du serveur Edge doit également être créée.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="0c4bd-111">Ports et protocoles de Director pour les définitions de pare-feu</span><span class="sxs-lookup"><span data-stu-id="0c4bd-111">Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c4bd-112">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="0c4bd-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="0c4bd-113">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="0c4bd-113">Source IP address</span></span></th>
<th><span data-ttu-id="0c4bd-114">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="0c4bd-114">Destination IP address</span></span></th>
<th><span data-ttu-id="0c4bd-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c4bd-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4bd-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="0c4bd-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-117">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="0c4bd-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-118">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="0c4bd-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-119">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée aux services Internet de Director HLB VIP et aux services Web des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4bd-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="0c4bd-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-121">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="0c4bd-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-122">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="0c4bd-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-123">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée aux services Internet de Director HLB VIP et aux services Web des serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Servers web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4bd-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="0c4bd-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-125">directeur</span><span class="sxs-lookup"><span data-stu-id="0c4bd-125">Director</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-126">Serveur frontal ou liste de front-end</span><span class="sxs-lookup"><span data-stu-id="0c4bd-126">Front End Server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-127">Communication entre serveur entre le directeur HLB VIP et les serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="0c4bd-127">Inter-server communication between the Director HLB VIP and the Front End Servers</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4bd-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="0c4bd-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-129">Clients internes</span><span class="sxs-lookup"><span data-stu-id="0c4bd-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-130">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="0c4bd-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-131">Le directeur fournit des services Web aux clients externes et internes.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4bd-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="0c4bd-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-133">Clients internes</span><span class="sxs-lookup"><span data-stu-id="0c4bd-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-134">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="0c4bd-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-135">Le directeur fournit des services Web aux clients externes et internes.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4bd-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="0c4bd-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-137">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="0c4bd-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-138">Adresse VIP de l’équilibrage de charge matérielle Director</span><span class="sxs-lookup"><span data-stu-id="0c4bd-138">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-139">Communication SIP du serveur Edge au directeur et aux serveurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="0c4bd-139">SIP communication from the Edge Server to the Director, and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4bd-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="0c4bd-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-141">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0c4bd-141">Any</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-142">directeur</span><span class="sxs-lookup"><span data-stu-id="0c4bd-142">Director</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-143">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="0c4bd-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4bd-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="0c4bd-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-145">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0c4bd-145">Any</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-146">directeur</span><span class="sxs-lookup"><span data-stu-id="0c4bd-146">Director</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-147">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="0c4bd-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4bd-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="0c4bd-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-149">Indifférente</span><span class="sxs-lookup"><span data-stu-id="0c4bd-149">Any</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-150">directeur</span><span class="sxs-lookup"><span data-stu-id="0c4bd-150">Director</span></span></p></td>
<td><p><span data-ttu-id="0c4bd-151">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClsAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="0c4bd-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0c4bd-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c4bd-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

