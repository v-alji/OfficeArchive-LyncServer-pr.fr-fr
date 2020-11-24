---
title: 'Lync Server 2013 : configuration requise pour DNS pour la connexion automatique au client'
description: 'Lync Server 2013 : configuration requise pour DNS pour la connexion automatique au client.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for automatic client sign-in
ms:assetid: 3bcd4bb3-a022-4ffa-b005-1a95ad2b1796
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425884(v=OCS.15)
ms:contentKeyID: 48183873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2247c955e0a563a22fb5d0ec20735291a836cdfc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395025"
---
# <a name="dns-requirements-for-automatic-client-sign-in-in-lync-server-2013"></a><span data-ttu-id="cbf37-103">Configuration DNS requise pour la connexion automatique au client dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cbf37-103">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cbf37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cbf37-104">

<span> </span></span></span>

<span data-ttu-id="cbf37-105">_**Dernière modification de la rubrique :** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="cbf37-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="cbf37-106">Cette section décrit les enregistrements DNS (Domain Name System) nécessaires à la connexion automatique du client.</span><span class="sxs-lookup"><span data-stu-id="cbf37-106">This section explains the Domain Name System (DNS) records that are required for automatic client sign-in.</span></span> <span data-ttu-id="cbf37-107">Lorsque vous déployez vos serveurs Standard Edition ou pools frontal, vous pouvez configurer vos clients de manière à utiliser la découverte automatique pour vous connecter au serveur Standard Edition Server ou au pool frontal approprié.</span><span class="sxs-lookup"><span data-stu-id="cbf37-107">When you deploy your Standard Edition servers or Front End pools, you can configure your clients to use automatic discovery to sign in to the appropriate Standard Edition server or Front End pool.</span></span> <span data-ttu-id="cbf37-108">Si vous envisagez de nécessiter la connexion manuelle de vos clients à Lync Server 2013, vous pouvez ignorer cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="cbf37-108">If you plan to require your clients to connect manually to Lync Server 2013, you can skip this topic.</span></span>

<span data-ttu-id="cbf37-109">Pour prendre en charge la connexion automatique au client, vous devez :</span><span class="sxs-lookup"><span data-stu-id="cbf37-109">To support automatic client sign-in, you must:</span></span>

  - <span data-ttu-id="cbf37-110">Désigner un serveur ou un pool unique pour distribuer et authentifier les demandes de connexion au client.</span><span class="sxs-lookup"><span data-stu-id="cbf37-110">Designate a single server or pool to distribute and authenticate client sign-in requests.</span></span> <span data-ttu-id="cbf37-111">Il peut s’agir d’un serveur ou d’un pool de votre organisation qui héberge des utilisateurs ou d’un serveur dédié ou d’un pool dédié à cette fin qui n’héberge aucun utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbf37-111">This can be an existing server or pool in your organization that hosts users, or you can designate a dedicated server or pool for this purpose that hosts no users.</span></span> <span data-ttu-id="cbf37-112">Pour une disponibilité élevée, nous vous recommandons de désigner un pool frontal pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="cbf37-112">For high availability, we recommend that you designate a Front End pool for this function.</span></span>

  - <span data-ttu-id="cbf37-113">Créer un enregistrement SRV DNS interne pour prendre en charge la connexion automatique du client pour ce serveur ou pool.</span><span class="sxs-lookup"><span data-stu-id="cbf37-113">Create an internal DNS SRV record to support automatic client sign-in for this server or pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cbf37-114">Dans les exigences d’enregistrement suivantes, le domaine SIP fait référence à la partie hôte des URI SIP attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cbf37-114">In the following record requirements, SIP domain refers to the host portion of the SIP URIs assigned to users.</span></span> <span data-ttu-id="cbf37-115">Par exemple, si les URI SIP sont du type \* @contoso. com, contoso.com est le domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="cbf37-115">For example, if SIP URIs are of the form \*@contoso.com, contoso.com is the SIP domain.</span></span> <span data-ttu-id="cbf37-116">Le domaine SIP est souvent différent du domaine interne d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbf37-116">The SIP domain is often different from the internal Active Directory domain.</span></span> <span data-ttu-id="cbf37-117">Une organisation peut également prendre en charge plusieurs domaines SIP.</span><span class="sxs-lookup"><span data-stu-id="cbf37-117">An organization can also support multiple SIP domains.</span></span>

    
    </div>

<span data-ttu-id="cbf37-118">Pour activer la configuration automatique pour vos clients, vous devez créer un enregistrement SRV DNS interne qui mappe l’un des enregistrements suivants au nom de domaine complet (FQDN) du pool frontal ou du serveur Standard Edition qui transmet les demandes de connexion aux clients Lync :</span><span class="sxs-lookup"><span data-stu-id="cbf37-118">To enable automatic configuration for your clients, you must create an internal DNS SRV record that maps one of the following records to the fully qualified domain name (FQDN) of the Front End pool or Standard Edition server that distributes sign-in requests from Lync clients:</span></span>

  - <span data-ttu-id="cbf37-119">\_sipinternaltls. \_ TCP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="cbf37-119">\_sipinternaltls.\_tcp.\<domain\></span></span> <span data-ttu-id="cbf37-120">-pour les connexions TLS internes</span><span class="sxs-lookup"><span data-stu-id="cbf37-120">- for internal TLS connections</span></span>

<span data-ttu-id="cbf37-121">Vous n’avez besoin de créer qu’un seul enregistrement SRV pour le pool frontal ou le serveur Standard Edition Server, ou la distribution de demandes de connexion.</span><span class="sxs-lookup"><span data-stu-id="cbf37-121">You only need to create a single SRV record for the Front End pool or Standard Edition server or that will distribute sign-in requests.</span></span>

<span data-ttu-id="cbf37-122">Le tableau suivant montre quelques exemples d’enregistrements nécessaires pour l’entreprise fictive contoso, qui prend en charge les domaines SIP de contoso.com et retail.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="cbf37-122">The following table shows some example records required for the fictitious company Contoso, which supports SIP domains of contoso.com and retail.contoso.com.</span></span>

### <a name="example-of-dns-records-required-for-automatic-client-sign-in-with-multiple-sip-domains"></a><span data-ttu-id="cbf37-123">Exemple d’enregistrements DNS requis pour la connexion automatique du client avec plusieurs domaines SIP</span><span class="sxs-lookup"><span data-stu-id="cbf37-123">Example of DNS Records Required for Automatic Client Sign-in with Multiple SIP Domains</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cbf37-124">Nom de domaine complet du pool frontal utilisé pour distribuer les demandes de connexion</span><span class="sxs-lookup"><span data-stu-id="cbf37-124">FQDN of Front End pool used to distribute sign-in requests</span></span></th>
<th><span data-ttu-id="cbf37-125">Domaine SIP</span><span class="sxs-lookup"><span data-stu-id="cbf37-125">SIP domain</span></span></th>
<th><span data-ttu-id="cbf37-126">Enregistrement DNS SRV</span><span class="sxs-lookup"><span data-stu-id="cbf37-126">DNS SRV record</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbf37-127">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-127">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="cbf37-128">contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-128">contoso.com</span></span></p></td>
<td><p><span data-ttu-id="cbf37-129">Un enregistrement SRV pour le domaine _sipinternaltls. _ TCP. contoso. com sur le port 5061 qui correspond à pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-129">An SRV record for _sipinternaltls._tcp.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbf37-130">pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-130">pool01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="cbf37-131">retail.contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-131">retail.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="cbf37-132">Un enregistrement SRV pour le domaine _sipinternaltls. _ TCP. Retail. contoso. com sur le port 5061 qui correspond à pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-132">An SRV record for _sipinternaltls._tcp.retail.contoso.com domain over port 5061 that maps to pool01.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="cbf37-133">Par défaut, les requêtes pour les enregistrements DNS respectent le strict rapprochement de nom de domaine entre le domaine figurant dans le nom d’utilisateur et l’enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="cbf37-133">By default, queries for DNS records adhere to strict domain name matching between the domain in the user name and the SRV record.</span></span> <span data-ttu-id="cbf37-134">Si vous préférez que les requêtes DNS du client utilisent plutôt une correspondance de suffixes, vous pouvez configurer la stratégie de groupe DisableStrictDNSNaming.</span><span class="sxs-lookup"><span data-stu-id="cbf37-134">If you prefer that client DNS queries use suffix matching instead, you can configure the DisableStrictDNSNaming Group Policy.</span></span> <span data-ttu-id="cbf37-135">Pour plus d’informations, reportez-vous à la section <A href="lync-server-2013-planning-for-clients-and-devices.md">planification des clients et des appareils dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="cbf37-135">For details, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="example-of-the-certificates-and-dns-records-required-for-automatic-client-sign-in"></a><span data-ttu-id="cbf37-136">Exemple de certificats et d’enregistrements DNS requis pour le client automatique Sign-In</span><span class="sxs-lookup"><span data-stu-id="cbf37-136">Example of the Certificates and DNS Records Required for Automatic Client Sign-In</span></span>

<span data-ttu-id="cbf37-137">Cet exemple utilise les mêmes noms d’exemples dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="cbf37-137">This example uses the same example names in the preceding table.</span></span> <span data-ttu-id="cbf37-138">L’organisation contoso prend en charge les domaines SIP de contoso.com et retail.contoso.com, et tous les utilisateurs ont un URI SIP dans l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cbf37-138">The Contoso organization supports the SIP domains of contoso.com and retail.contoso.com, and all of its users have a SIP URI in one of the following forms:</span></span>

  - <span data-ttu-id="cbf37-139">\<user\>@retail. contoso.com</span><span class="sxs-lookup"><span data-stu-id="cbf37-139">\<user\>@retail.contoso.com</span></span>

  - <span data-ttu-id="cbf37-140">\<user\>@contoso. com</span><span class="sxs-lookup"><span data-stu-id="cbf37-140">\<user\>@contoso.com</span></span>

<span data-ttu-id="cbf37-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cbf37-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

