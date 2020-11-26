---
title: 'Lync Server 2013 : Résumé du certificat-découverte automatique'
description: 'Lync Server 2013 : Résumé du certificat-découverte automatique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Autodiscover
ms:assetid: 16ac96bb-882a-4141-b75c-9530637548d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945616(v=OCS.15)
ms:contentKeyID: 51541451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae421401421434a4c4069c1d90ee287dfb016997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435348"
---
# <a name="certificate-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="dd5df-103">Résumé du certificat-découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd5df-103">Certificate summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd5df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd5df-104">

<span> </span></span></span>

<span data-ttu-id="dd5df-105">_**Dernière modification de la rubrique :** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="dd5df-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="dd5df-106">Le service de découverte automatique de Lync Server 2013 s’exécute sur le directeur et les serveurs du pool frontal, et lorsqu’il est publié en DNS, il est possible d’utiliser les clients Lync pour localiser les services de serveur et d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd5df-106">The Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by Lync clients to locate server and user services.</span></span> <span data-ttu-id="dd5df-107">Si vous effectuez une mise à niveau à partir de Lync Server 2010 et que vous n’avez pas déployé de mobilité, pour que les clients puissent utiliser la découverte automatique, vous devez modifier les listes de noms de remplacement du sujet du certificat sur tout directeur et serveur frontal exécutant le service de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="dd5df-107">If you are upgrading from Lync Server 2010 and did not deploy Mobility, before clients can use automatic discovery, you must modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="dd5df-108">Par ailleurs, il est possible que vous deviez modifier les listes nom de remplacement de l’objet sur les certificats utilisés pour les règles de publication de service Web externe sur les proxys inverses.</span><span class="sxs-lookup"><span data-stu-id="dd5df-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="dd5df-109">La décision concernant l’utilisation des listes de noms de substitution sur les proxys inverse est basée sur le fait que vous publiez le service de découverte automatique sur le port 80 ou sur le port 443 :</span><span class="sxs-lookup"><span data-stu-id="dd5df-109">The decision about whether to use subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="dd5df-110">**Publié sur le port 80**   Aucune modification de certificat n’est requise si la requête initiale du service de découverte automatique a lieu sur le port 80.</span><span class="sxs-lookup"><span data-stu-id="dd5df-110">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="dd5df-111">En effet, les appareils mobiles exécutant Lync accèdent au proxy inverse sur le port 80 en externe, puis ils sont connectés à un serveur directeur ou frontal sur le port 8080 en interne.</span><span class="sxs-lookup"><span data-stu-id="dd5df-111">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be bridged to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="dd5df-112">Pour plus d’informations, consultez la section exigences techniques de découverte automatique à l’aide de port 80» [pour la mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="dd5df-112">For details, see the "Initial Autodiscover Process Using Port 80" section [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="dd5df-113">**Publié sur le port 443**   La liste autre nom de l’objet sur les certificats utilisés par la règle de publication des services Web externes doit contenir un *lyncdiscover. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="dd5df-113">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="dd5df-114">entrée pour chaque domaine SIP au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dd5df-114">entry for each SIP domain within your organization.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dd5df-115">Nous vous recommandons vivement d’utiliser HTTPs sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="dd5df-115">We highly recommend using HTTPS over HTTP.</span></span> <span data-ttu-id="dd5df-116">HTTPs utilise des certificats pour chiffrer le trafic.</span><span class="sxs-lookup"><span data-stu-id="dd5df-116">HTTPS uses certificates to encrypt traffic.</span></span> <span data-ttu-id="dd5df-117">HTTP ne permet pas d’effectuer le chiffrement et les données envoyées seront au format texte brut.</span><span class="sxs-lookup"><span data-stu-id="dd5df-117">HTTP does not provide for encryption, and any data sent will be plain text.</span></span>

    
    </div>

<span data-ttu-id="dd5df-118">La réémission de certificats à l’aide d’une autorité de certification interne est généralement un processus simple.</span><span class="sxs-lookup"><span data-stu-id="dd5df-118">Reissuing certificates by using an internal certificate authority is typically a simple process.</span></span> <span data-ttu-id="dd5df-119">En revanche, pour les certificats publics utilisés sur la règle de publication de service Web, l’ajout de plusieurs entrées de nom de domaine alternatif peut devenir coûteux.</span><span class="sxs-lookup"><span data-stu-id="dd5df-119">But for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="dd5df-120">Pour contourner ce problème, nous prenons en charge la connexion automatique de découverte automatique sur le port 80, qui est ensuite redirigée vers le port 8080 du directeur ou du serveur principal.</span><span class="sxs-lookup"><span data-stu-id="dd5df-120">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dd5df-121">Si votre infrastructure Lync Server 2013 utilise des certificats internes émis par une autorité de certification interne et que vous envisagez de prendre en charge les appareils mobiles qui se connectent sans fil, soit la chaîne de certificats racine de l’autorité de certification interne doit être installée sur les appareils mobiles, soit vous devez utiliser un certificat public sur votre infrastructure Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dd5df-121">If your Lync Server 2013 infrastructure uses internal certificates that are issued from an internal certification authority (CA) and you plan to support mobile devices connecting wirelessly, either the root certificate chain from the internal CA must be installed on the mobile devices or you must change to a public certificate on your Lync Server 2013 infrastructure.</span></span>



</div>

<span data-ttu-id="dd5df-122">Cette rubrique décrit les noms de remplacement d’objet ajoutés requis pour le directeur, le serveur frontal et le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="dd5df-122">This topic describes the added subject alternative names required for the Director, Front End Server and reverse proxy.</span></span> <span data-ttu-id="dd5df-123">Seuls les noms d’autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="dd5df-123">Only the added subject alternative names (SAN) are referenced.</span></span> <span data-ttu-id="dd5df-124">Reportez-vous aux sections planification pour plus d’informations sur les autres entrées des certificats.</span><span class="sxs-lookup"><span data-stu-id="dd5df-124">Refer to the planning sections for guidance on the other entries on certificates.</span></span> <span data-ttu-id="dd5df-125">Pour plus d’informations, reportez-vous à [la rubrique scénarios pour le directeur dans Lync server 2013](lync-server-2013-scenarios-for-the-director.md), [scénarios d’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md)et [scénarios de proxy inverse dans Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="dd5df-125">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md), [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md), and [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span></span>

<span data-ttu-id="dd5df-126">Les tableaux suivants définissent les entrées du SAN de découverte automatique pour le pool de directeurs, le pool frontal et le proxy inverse :</span><span class="sxs-lookup"><span data-stu-id="dd5df-126">The following tables define the Autodiscover SAN entries for the Director pool, the Front End pool, and the reverse proxy:</span></span>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="dd5df-127">Conditions requises pour le certificat de pool de réalisateur</span><span class="sxs-lookup"><span data-stu-id="dd5df-127">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd5df-128">Description</span><span class="sxs-lookup"><span data-stu-id="dd5df-128">Description</span></span></th>
<th><span data-ttu-id="dd5df-129">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="dd5df-129">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd5df-130">URL du service de découverte automatique interne</span><span class="sxs-lookup"><span data-stu-id="dd5df-130">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="dd5df-131">SAN = lyncdiscoverinternal. &lt; nom de domaine interne&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-131">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd5df-132">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="dd5df-132">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="dd5df-133">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-133">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="dd5df-134">Vous attribuez le certificat qui vient d’être mis à jour avec la nouvelle entrée SAN au certificat par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd5df-134">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="dd5df-135">Vous pouvez également utiliser le SAN = \*. &lt; sipdomain &gt; .</span><span class="sxs-lookup"><span data-stu-id="dd5df-135">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;.</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="dd5df-136">Conditions requises pour le certificat de pool frontal</span><span class="sxs-lookup"><span data-stu-id="dd5df-136">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd5df-137">Description</span><span class="sxs-lookup"><span data-stu-id="dd5df-137">Description</span></span></th>
<th><span data-ttu-id="dd5df-138">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="dd5df-138">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd5df-139">URL du service de découverte automatique interne</span><span class="sxs-lookup"><span data-stu-id="dd5df-139">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="dd5df-140">SAN = lyncdiscoverinternal. &lt; nom de domaine interne&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-140">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd5df-141">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="dd5df-141">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="dd5df-142">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-142">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="dd5df-143">Vous attribuez le certificat qui vient d’être mis à jour avec la nouvelle entrée SAN au certificat par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd5df-143">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="dd5df-144">Vous pouvez également utiliser le SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-144">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="dd5df-145">Conditions requises pour les certificats de proxy inverse (AC publique)</span><span class="sxs-lookup"><span data-stu-id="dd5df-145">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd5df-146">Description</span><span class="sxs-lookup"><span data-stu-id="dd5df-146">Description</span></span></th>
<th><span data-ttu-id="dd5df-147">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="dd5df-147">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd5df-148">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="dd5df-148">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="dd5df-149">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="dd5df-149">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="dd5df-150">Vous attribuez le certificat récemment mis à jour avec la nouvelle entrée SAN à l’écouteur SSL du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="dd5df-150">You assign the newly updated certificate with the new SAN entry to the SSL Listener on the reverse proxy.</span></span>



<span data-ttu-id="dd5df-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd5df-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

