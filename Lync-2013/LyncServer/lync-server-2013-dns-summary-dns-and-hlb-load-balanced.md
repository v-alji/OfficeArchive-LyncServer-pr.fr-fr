---
title: 'Lync Server 2013 : Résumé des enregistrements DNS - Équilibrage de charge DNS et matérielle'
description: 'Serveur de synthèse de Lync Server 2013 : DNS et HLB de répartition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - DNS and HLB load balanced
ms:assetid: d2132695-1956-4190-a98e-cd7255cbded6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205273(v=OCS.15)
ms:contentKeyID: 48185447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c191d653ce4025618e135b4c69bc673f79a6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437741"
---
# <a name="dns-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="f62fd-103">Résumé des enregistrements DNS - Équilibrage de charge DNS et matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f62fd-103">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f62fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f62fd-104">

<span> </span></span></span>

<span data-ttu-id="f62fd-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="f62fd-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="f62fd-106">Le tableau suivant contient un résumé des enregistrements DNS requis pour prendre en charge le système de répartition de charge DNS et le directeur équilibré de charge matérielle.</span><span class="sxs-lookup"><span data-stu-id="f62fd-106">The following table contains a summary of the DNS records that are required to support the DNS load balanced and hardware load balanced Director.</span></span> <span data-ttu-id="f62fd-107">Le rôle du directeur nécessite des enregistrements DNS similaires comme serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="f62fd-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="f62fd-108">Le nombre d’enregistrements nécessaires est reflété dans les autres noms d’objet requis sur le certificat de réalisateur.</span><span class="sxs-lookup"><span data-stu-id="f62fd-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="f62fd-109">Différent du serveur frontal, le pool de directeurs n’héberge pas les comptes d’utilisateurs ou n’héberge pas les services de mobilité.</span><span class="sxs-lookup"><span data-stu-id="f62fd-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-dns-load-balancing-and-hardware-load-balancer"></a><span data-ttu-id="f62fd-110">Enregistrements DNS requis pour le pool de directeurs à l’aide de l’équilibrage de charge DNS et de l’équilibrage de charge matérielle</span><span class="sxs-lookup"><span data-stu-id="f62fd-110">DNS Records Required for the Director Pool using DNS Load Balancing and Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f62fd-111">Emplacement/TYPE/port</span><span class="sxs-lookup"><span data-stu-id="f62fd-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="f62fd-112">Nom de domaine complet/enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="f62fd-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="f62fd-113">IP address/FQDN</span><span class="sxs-lookup"><span data-stu-id="f62fd-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="f62fd-114">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="f62fd-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f62fd-115">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f62fd-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="f62fd-117">directeur</span><span class="sxs-lookup"><span data-stu-id="f62fd-117">Director</span></span></p></td>
<td><p><span data-ttu-id="f62fd-118">Enregistrement hôte de Director utilisé pour la réplication et le serveur vers serveur</span><span class="sxs-lookup"><span data-stu-id="f62fd-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f62fd-119">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f62fd-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="f62fd-121">pool de directeurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-121">Director pool</span></span></p></td>
<td><p><span data-ttu-id="f62fd-122">Enregistrement hôte du pool de directeurs d’équilibrage de charge DNS pour serveur à serveur</span><span class="sxs-lookup"><span data-stu-id="f62fd-122">Host record for the DNS load balanced Director pool for server to server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f62fd-123">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f62fd-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f62fd-125">pool de directeurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-125">Director pool</span></span></p></td>
<td><p><span data-ttu-id="f62fd-126">Protocole SIP (Session Initiation Protocol) à partir de l’interface interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="f62fd-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f62fd-127">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f62fd-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f62fd-129">HLB VIP du pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="f62fd-130">Équilibrage de charge matérielle publié services Web de numérotation à partir du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="f62fd-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f62fd-131">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f62fd-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f62fd-133">HLB VIP du pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="f62fd-134">Équilibrage de charge matérielle publié avec les services Web à partir du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="f62fd-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f62fd-135">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="f62fd-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f62fd-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f62fd-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f62fd-137">HLB VIP du pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="f62fd-138">Équilibrage de la charge matérielle publié et définie par les services Web externes du ticket de proxy inverse pour le pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="f62fd-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f62fd-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f62fd-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

