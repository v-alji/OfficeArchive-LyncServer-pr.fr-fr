---
title: 'Lync Server 2013 : configuration requise pour la mobilité'
description: 'Lync Server 2013 : configuration requise pour la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437804"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="ef191-103">Configuration DNS requise pour la mobilité avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ef191-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ef191-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ef191-104">

<span> </span></span></span>

<span data-ttu-id="ef191-105">_**Dernière modification de la rubrique :** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="ef191-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="ef191-106">Lorsque vous déployez la fonctionnalité de mobilité de Lync Server 2013, vous pouvez utiliser les nouvelles URL disponibles avec le service de découverte automatique Microsoft Lync Server 2013 ou utiliser vos URL de services Web existantes.</span><span class="sxs-lookup"><span data-stu-id="ef191-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="ef191-107">Si vous utilisez vos URL existantes, les utilisateurs doivent entrer manuellement les URL dans leurs paramètres d’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="ef191-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="ef191-108">Cette option est généralement utilisée pour la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="ef191-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="ef191-109">Lorsque vous utilisez les nouvelles URL, les clients mobiles peuvent automatiquement découvrir les ressources de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ef191-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="ef191-110">Lorsque vous prenez en charge la découverte automatique, vous devez ajouter de nouveaux enregistrements DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="ef191-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="ef191-111">Cette section décrit les enregistrements DNS requis pour la découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="ef191-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="ef191-112">Pour prendre en charge la découverte automatique, vous devez créer les enregistrements DNS suivants pour chaque domaine SIP :</span><span class="sxs-lookup"><span data-stu-id="ef191-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="ef191-113">Un enregistrement DNS interne pour prendre en charge les utilisateurs mobiles qui se connectent au sein du réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ef191-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="ef191-114">Enregistrement DNS externe ou public permettant de prendre en charge les utilisateurs mobiles qui se connectent à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="ef191-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="ef191-115">L’URL de découverte automatique interne ne doit pas être adressable depuis l’extérieur de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="ef191-115">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="ef191-116">L’URL de découverte automatique externe ne doit pas être adressable à partir de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="ef191-116">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="ef191-117">Toutefois, si vous ne pouvez pas respecter cette exigence pour l’URL externe, le client mobile ne doit pas être affecté.</span><span class="sxs-lookup"><span data-stu-id="ef191-117">However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="ef191-118">Les enregistrements DNS peuvent être des enregistrements CNAMe ou des enregistrements (Host).</span><span class="sxs-lookup"><span data-stu-id="ef191-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="ef191-119">**Enregistrements DNS internes**</span><span class="sxs-lookup"><span data-stu-id="ef191-119">**Internal DNS records**</span></span>

<span data-ttu-id="ef191-120">Vous devez créer un des enregistrements DNS internes suivants :</span><span class="sxs-lookup"><span data-stu-id="ef191-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef191-121">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ef191-121">Record type</span></span></th>
<th><span data-ttu-id="ef191-122">Nom d’hôte ou définition SRV</span><span class="sxs-lookup"><span data-stu-id="ef191-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="ef191-123">Résolu en</span><span class="sxs-lookup"><span data-stu-id="ef191-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef191-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="ef191-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="ef191-125">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="ef191-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="ef191-126">Nom de domaine complet des services Web internes (FQDN) de votre pool de directeurs, le cas échéant, ou de votre pool frontal si vous n’avez pas de réalisateur</span><span class="sxs-lookup"><span data-stu-id="ef191-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef191-127">A (hôte)</span><span class="sxs-lookup"><span data-stu-id="ef191-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="ef191-128">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="ef191-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="ef191-129">Adresse IP des services Web internes (adresse IP virtuelle) si vous utilisez un équilibreur de charge, si vous en avez un, ou si vous n’avez pas de directeur...</span><span class="sxs-lookup"><span data-stu-id="ef191-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ef191-130">**Enregistrements DNS externes**</span><span class="sxs-lookup"><span data-stu-id="ef191-130">**External DNS records**</span></span>

<span data-ttu-id="ef191-131">Vous devez créer un des enregistrements DNS externes suivants :</span><span class="sxs-lookup"><span data-stu-id="ef191-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef191-132">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ef191-132">Record type</span></span></th>
<th><span data-ttu-id="ef191-133">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="ef191-133">Host name</span></span></th>
<th><span data-ttu-id="ef191-134">Résolu en</span><span class="sxs-lookup"><span data-stu-id="ef191-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef191-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="ef191-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="ef191-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="ef191-136">lyncdiscover.</span></span> <span data-ttu-id="ef191-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="ef191-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="ef191-138">Nom de domaine complet des services Web externes pour votre pool de directeurs, le cas échéant, ou pour votre pool frontal si vous n’avez pas de réalisateur</span><span class="sxs-lookup"><span data-stu-id="ef191-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef191-139">A (hôte)</span><span class="sxs-lookup"><span data-stu-id="ef191-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="ef191-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="ef191-140">lyncdiscover.</span></span> <span data-ttu-id="ef191-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="ef191-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="ef191-142">Adresse IP externe ou publique (adresse VIP si vous utilisez un équilibreur de charge) du proxy inverse</span><span class="sxs-lookup"><span data-stu-id="ef191-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef191-143">SRV</span><span class="sxs-lookup"><span data-stu-id="ef191-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="ef191-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="ef191-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="ef191-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="ef191-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="ef191-146">Se résout en enregistrement Host (A ou AAAA) pour le service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="ef191-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="ef191-147">Pour prendre en charge les services de notifications de transmission et de notifications de type Apple, vous devez créer un enregistrement SRV pour chaque domaine SIP doté de clients mobiles Microsoft Lync.</span><span class="sxs-lookup"><span data-stu-id="ef191-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="ef191-148">Cette condition s’applique uniquement aux clients mobiles Microsoft Lync sur les appareils mobiles Apple ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ef191-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="ef191-149">Les appareils Android et Nokia Symbian n’utilisent pas la notification de transmission.</span><span class="sxs-lookup"><span data-stu-id="ef191-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="ef191-150">Lyncdiscover, également connu sous le nom de découverte automatique, le trafic passe par le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="ef191-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="ef191-151">Un enregistrement SRV pointe vers un enregistrement qui est résolu par le biais du service Edge d’accès.</span><span class="sxs-lookup"><span data-stu-id="ef191-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="ef191-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ef191-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

