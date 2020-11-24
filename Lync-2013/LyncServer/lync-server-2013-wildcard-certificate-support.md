---
title: Prise en charge des certificats comportant des caractères génériques Lync Server 2013
description: Prise en charge de certificat générique de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394469"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="faa52-103">Prise en charge des certificats comportant des caractères génériques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faa52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faa52-104">

<span> </span></span></span>

<span data-ttu-id="faa52-105">_**Dernière modification de la rubrique :** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="faa52-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="faa52-106">Lync Server 2013 utilise des certificats pour le chiffrement des communications et l’authentification par identité du serveur.</span><span class="sxs-lookup"><span data-stu-id="faa52-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="faa52-107">Dans certains cas, par exemple, la publication sur le Web par le biais du proxy inverse, l’entrée de nouveau nom de l’élément de nom de domaine complet (FQDN) du serveur qui présente le service n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="faa52-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="faa52-108">Dans ces cas-là, vous pouvez utiliser des certificats à l’aide d’entrées génériques pour réduire le coût d’un certificat demandé auprès d’une autorité de certification publique et réduire la complexité du processus de planification des certificats.</span><span class="sxs-lookup"><span data-stu-id="faa52-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="faa52-109">Pour conserver la fonctionnalité de périphériques de communications unifiées (UC) (par exemple, les téléphones de bureau), vous devez tester soigneusement le certificat déployé pour vous assurer que les appareils fonctionnent correctement après l’implémentation d’un certificat générique.</span><span class="sxs-lookup"><span data-stu-id="faa52-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="faa52-110">Il n’y a pas de prise en charge d’une entrée de caractère générique comme nom de sujet (également appelé nom commun ou NC) pour n’importe quel rôle.</span><span class="sxs-lookup"><span data-stu-id="faa52-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="faa52-111">Les rôles de serveur suivants sont pris en charge lorsque vous utilisez des entrées de caractères génériques dans le SAN :</span><span class="sxs-lookup"><span data-stu-id="faa52-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-112">**Proxy inverse.**</span><span class="sxs-lookup"><span data-stu-id="faa52-112">**Reverse proxy.**</span></span>   <span data-ttu-id="faa52-113">L’entrée SAN générique est prise en charge pour les certificats de publication d’URL simples (de conférence et de numérotation).</span><span class="sxs-lookup"><span data-stu-id="faa52-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-114">**Proxy inverse.**</span><span class="sxs-lookup"><span data-stu-id="faa52-114">**Reverse proxy.**</span></span>   <span data-ttu-id="faa52-115">L’entrée SAN générique est prise en charge pour les entrées du SAN pour LyncDiscover sur le certificat de publication.</span><span class="sxs-lookup"><span data-stu-id="faa52-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-116">**Méta.**</span><span class="sxs-lookup"><span data-stu-id="faa52-116">**Director.**</span></span>   <span data-ttu-id="faa52-117">L’entrée SAN générique est prise en charge pour les URL simples (réunion et numéro de téléphone) et pour les entrées SAN pour LyncDiscover et LyncDiscoverInternal dans les composants Web Director.</span><span class="sxs-lookup"><span data-stu-id="faa52-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-118">**Serveur frontal (édition standard) et liste frontale (Enterprise Edition).**</span><span class="sxs-lookup"><span data-stu-id="faa52-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="faa52-119">L’entrée SAN générique est prise en charge pour les URL simples (réunion et numéro de téléphone) et pour les entrées SAN pour LyncDiscover et LyncDiscoverInternal dans les composants webend Web.</span><span class="sxs-lookup"><span data-stu-id="faa52-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-120">**Exchange Unified Messaging (UM).**</span><span class="sxs-lookup"><span data-stu-id="faa52-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="faa52-121">Le serveur n’utilise pas d’entrées du SAN lorsqu’il est déployé en tant que serveur autonome.</span><span class="sxs-lookup"><span data-stu-id="faa52-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-122">**Serveur d’accès au client Microsoft Exchange Server.**</span><span class="sxs-lookup"><span data-stu-id="faa52-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="faa52-123">Les entrées génériques du SAN sont prises en charge pour les clients internes et externes.</span><span class="sxs-lookup"><span data-stu-id="faa52-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="faa52-124">**Exchange Unified Messaging (MU) et serveur d’accès au client Exchange Server sur le même serveur.**</span><span class="sxs-lookup"><span data-stu-id="faa52-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="faa52-125">Les entrées génériques du SAN sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="faa52-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="faa52-126">Rôles de serveur non mentionnés dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="faa52-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="faa52-127">Rôles de serveur internes (y compris, mais sans s’y limiter, le serveur de médiation, l’archivage et la surveillance du serveur, de l’unité de branchement survivant ou du serveur de succursales survivant)</span><span class="sxs-lookup"><span data-stu-id="faa52-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="faa52-128">Interfaces de serveur Edge externes</span><span class="sxs-lookup"><span data-stu-id="faa52-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="faa52-129">Serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="faa52-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="faa52-130">Pour l’interface du serveur Edge interne, une entrée générique peut être affectée au SAN et est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="faa52-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="faa52-131">Le SAN sur le serveur Edge interne n’est pas interrogé, et une entrée SAN générique a une valeur limitée.</span><span class="sxs-lookup"><span data-stu-id="faa52-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="faa52-132">Pour plus d’informations sur les configurations de certificats, y compris l’utilisation de caractères génériques dans les certificats, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="faa52-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="faa52-133">Exigences de certificat pour les serveurs internes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="faa52-134">Certificats requis pour l’accès des utilisateurs externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="faa52-135">Résumé des certificats - Équilibrage de charge DNS et matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="faa52-136">Résumé des certificats - Directeur unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="faa52-137">Résumé des certificats - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="faa52-138">Résumé des certificats - Proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="faa52-139">Instructions d’intégration de la messagerie unifiée locale et de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa52-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="faa52-140">Pour plus d’informations sur la configuration des certificats pour Exchange, y compris l’utilisation de caractères génériques, voir la documentation du produit Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="faa52-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="faa52-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faa52-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

