---
title: 'Lync Server 2013 : Résumé des enregistrements DNS - Un directeur'
description: 'Lync Server 2013 : DNS Summary-Director unique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78ef19383df45644ad951ca5da69ef893b231980
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393820"
---
# <a name="dns-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="77060-103">Résumé des enregistrements DNS - Un directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77060-103">DNS summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77060-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77060-104">

<span> </span></span></span>

<span data-ttu-id="77060-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="77060-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="77060-106">Le tableau suivant contient un résumé des enregistrements DNS requis pour la prise en charge du réalisateur unique.</span><span class="sxs-lookup"><span data-stu-id="77060-106">The following table contains a summary of the DNS records that are required to support the single Director.</span></span> <span data-ttu-id="77060-107">Le rôle du directeur nécessite des enregistrements DNS similaires comme serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="77060-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="77060-108">Le nombre d’enregistrements nécessaires est reflété dans les autres noms d’objet requis sur le certificat de réalisateur.</span><span class="sxs-lookup"><span data-stu-id="77060-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="77060-109">Différent du serveur frontal, le directeur n’héberge pas les comptes d’utilisateurs ou n’héberge pas les services de mobilité.</span><span class="sxs-lookup"><span data-stu-id="77060-109">Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director"></a><span data-ttu-id="77060-110">Enregistrements DNS requis pour le directeur</span><span class="sxs-lookup"><span data-stu-id="77060-110">DNS Records Required for the Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77060-111">Emplacement/TYPE/port</span><span class="sxs-lookup"><span data-stu-id="77060-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="77060-112">Nom de domaine complet/enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="77060-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="77060-113">IP address/FQDN</span><span class="sxs-lookup"><span data-stu-id="77060-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="77060-114">Cartes sur/Commentaires</span><span class="sxs-lookup"><span data-stu-id="77060-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77060-115">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="77060-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="77060-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="77060-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="77060-117">directeur</span><span class="sxs-lookup"><span data-stu-id="77060-117">Director</span></span></p></td>
<td><p><span data-ttu-id="77060-118">Enregistrement hôte de Director utilisé pour la réplication et le serveur vers serveur</span><span class="sxs-lookup"><span data-stu-id="77060-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77060-119">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="77060-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="77060-120">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="77060-120">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="77060-121">directeur</span><span class="sxs-lookup"><span data-stu-id="77060-121">Director</span></span></p></td>
<td><p><span data-ttu-id="77060-122">Protocole SIP (Session Initiation Protocol) à partir de l’interface latérale interne du serveur Edge</span><span class="sxs-lookup"><span data-stu-id="77060-122">Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77060-123">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="77060-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="77060-124">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="77060-124">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="77060-125">directeur</span><span class="sxs-lookup"><span data-stu-id="77060-125">Director</span></span></p></td>
<td><p><span data-ttu-id="77060-126">A publié les services Web de numérotation à partir du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="77060-126">Published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77060-127">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="77060-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="77060-128">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="77060-128">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="77060-129">directeur</span><span class="sxs-lookup"><span data-stu-id="77060-129">Director</span></span></p></td>
<td><p><span data-ttu-id="77060-130">Publié les services Web à partir du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="77060-130">Published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77060-131">DNS interne/A</span><span class="sxs-lookup"><span data-stu-id="77060-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="77060-132">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="77060-132">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="77060-133">directeur</span><span class="sxs-lookup"><span data-stu-id="77060-133">Director</span></span></p></td>
<td><p><span data-ttu-id="77060-134">Publié et défini par les services Web externes du proxy inverse pour le directeur</span><span class="sxs-lookup"><span data-stu-id="77060-134">Published and defined by the reverse proxy Web Ticket external web services for the Director</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="77060-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77060-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

