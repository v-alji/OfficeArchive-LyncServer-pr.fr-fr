---
title: 'Lync Server 2013 : Résumé des ports - Directeur unique'
description: 'Lync Server 2013 : Résumé de port-Director unique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436978"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="03f90-103">Résumé des ports - Directeur unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03f90-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03f90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03f90-104">

<span> </span></span></span>

<span data-ttu-id="03f90-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="03f90-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="03f90-106">La configuration requise pour les ports de pare-feu pour un seul directeur consiste à utiliser les ports utilisés pour établir une communication avec le directeur à partir de l’interface interne ou du réseau interne du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="03f90-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="03f90-107">Microsoft Lync Server 2013 par défaut s’attend à ce que les ports HTTP/TCP 8080 et HTTPs/TCP 4443 soient ouverts du proxy inverse au directeur, ainsi qu’au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="03f90-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="03f90-108">Par ailleurs, il doit y avoir une communication SIP (Session Initiation Protocol) à partir de l’interface interne du serveur Edge au directeur et au serveur principal et au pool frontal.</span><span class="sxs-lookup"><span data-stu-id="03f90-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="03f90-109">Le protocole SIP utilise SIP/MTLS/TCP 5061 du serveur Edge au pool frontal et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="03f90-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="03f90-110">Une règle qui autorise la communication SIP/MTLS/TCP 5061 à partir du réalisateur, du pool frontal et du serveur frontal vers l’interface interne du serveur Edge doit également être créée.</span><span class="sxs-lookup"><span data-stu-id="03f90-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="03f90-111">Ports et protocoles de Director uniques pour les définitions de pare-feu</span><span class="sxs-lookup"><span data-stu-id="03f90-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03f90-112">Rôles/protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="03f90-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="03f90-113">Adresse IP source</span><span class="sxs-lookup"><span data-stu-id="03f90-113">Source IP address</span></span></th>
<th><span data-ttu-id="03f90-114">Adresse IP de destination</span><span class="sxs-lookup"><span data-stu-id="03f90-114">Destination IP address</span></span></th>
<th><span data-ttu-id="03f90-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="03f90-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03f90-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="03f90-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="03f90-117">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="03f90-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-118">directeur</span><span class="sxs-lookup"><span data-stu-id="03f90-118">Director</span></span></p></td>
<td><p><span data-ttu-id="03f90-119">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée au directeur et aux services Web du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="03f90-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f90-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="03f90-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="03f90-121">Interface interne du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="03f90-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-122">directeur</span><span class="sxs-lookup"><span data-stu-id="03f90-122">Director</span></span></p></td>
<td><p><span data-ttu-id="03f90-123">Initialement reçues par le côté extérieur du proxy inverse, la communication est envoyée au directeur et aux services Web du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="03f90-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03f90-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="03f90-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="03f90-125">directeur</span><span class="sxs-lookup"><span data-stu-id="03f90-125">Director</span></span></p></td>
<td><p><span data-ttu-id="03f90-126">Serveur frontal ou liste de front-end</span><span class="sxs-lookup"><span data-stu-id="03f90-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="03f90-127">Communication entre serveur entre le directeur et le serveur frontal</span><span class="sxs-lookup"><span data-stu-id="03f90-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f90-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="03f90-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="03f90-129">Clients internes</span><span class="sxs-lookup"><span data-stu-id="03f90-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="03f90-130">Services Web de Director</span><span class="sxs-lookup"><span data-stu-id="03f90-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="03f90-131">Le directeur fournit des services Web aux clients internes et externes.</span><span class="sxs-lookup"><span data-stu-id="03f90-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03f90-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="03f90-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="03f90-133">Clients internes</span><span class="sxs-lookup"><span data-stu-id="03f90-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="03f90-134">Services Web de Director</span><span class="sxs-lookup"><span data-stu-id="03f90-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="03f90-135">Le directeur fournit des services Web aux clients internes et externes.</span><span class="sxs-lookup"><span data-stu-id="03f90-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f90-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="03f90-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="03f90-137">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="03f90-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-138">directeur</span><span class="sxs-lookup"><span data-stu-id="03f90-138">Director</span></span></p></td>
<td><p><span data-ttu-id="03f90-139">Communication SIP du serveur Edge au directeur et au serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="03f90-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03f90-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="03f90-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="03f90-141">Indifférente</span><span class="sxs-lookup"><span data-stu-id="03f90-141">Any</span></span></p></td>
<td><p><span data-ttu-id="03f90-142">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="03f90-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-143">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClasAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="03f90-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f90-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="03f90-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="03f90-145">Indifférente</span><span class="sxs-lookup"><span data-stu-id="03f90-145">Any</span></span></p></td>
<td><p><span data-ttu-id="03f90-146">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="03f90-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-147">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClasAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="03f90-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03f90-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="03f90-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="03f90-149">Indifférente</span><span class="sxs-lookup"><span data-stu-id="03f90-149">Any</span></span></p></td>
<td><p><span data-ttu-id="03f90-150">Interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="03f90-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="03f90-151">Commandes du contrôleur du service de journalisation centralisées (ClsController.exe) ou de l’agent (ClasAgent.exe) et collection de journaux</span><span class="sxs-lookup"><span data-stu-id="03f90-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="03f90-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03f90-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

