---
title: 'Lync Server 2013 : Exigences relatives aux certificats pour la mobilité'
description: 'Lync Server 2013 : exigences relatives aux certificats pour la mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435361"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="e37e8-103">Exigences relatives aux certificats pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e37e8-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e37e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e37e8-104">

<span> </span></span></span>

<span data-ttu-id="e37e8-105">_**Dernière modification de la rubrique :** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="e37e8-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="e37e8-106">Si vous déployez la fonctionnalité de mobilité et que vous prenez en charge la découverte automatique pour les clients mobiles, vous devez inclure certaines entrées de nom alternatif de sujet sur les certificats pour la prise en charge de connexions sécurisées à partir des clients mobiles.</span><span class="sxs-lookup"><span data-stu-id="e37e8-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="e37e8-107">Vous devez inclure les autres entrées de nom de l’objet pour la découverte automatique sur les certificats suivants :</span><span class="sxs-lookup"><span data-stu-id="e37e8-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="e37e8-108">pool de directeurs</span><span class="sxs-lookup"><span data-stu-id="e37e8-108">Director pool</span></span>

  - <span data-ttu-id="e37e8-109">pool de serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="e37e8-109">Front End pool</span></span>

  - <span data-ttu-id="e37e8-110">Proxy inverse</span><span class="sxs-lookup"><span data-stu-id="e37e8-110">Reverse proxy</span></span>

<span data-ttu-id="e37e8-111">Cette section décrit les entrées de nom alternatif requises sur vos certificats pour une découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="e37e8-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e37e8-112">La réémission de certificats à l’aide d’une autorité de certification interne correspond généralement à un processus simple, mais l’ajout de plusieurs entrées de nom de remplacement de sujet à des certificats publics utilisés par le proxy inverse peut être coûteux.</span><span class="sxs-lookup"><span data-stu-id="e37e8-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="e37e8-113">Si vous avez de nombreux domaines SIP, le fait d’ajouter des noms de substitution d’objet très coûteux, vous pouvez configurer le proxy inverse pour qu’il utilise HTTP pour la demande de service de découverte automatique initiale au lieu d’utiliser HTTPs (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="e37e8-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="e37e8-114">Pour plus d’informations, voir <A href="lync-server-2013-technical-requirements-for-mobility.md">Configuration requise pour la mobilité dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="e37e8-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="e37e8-115">Conditions requises pour le certificat de pool de réalisateur</span><span class="sxs-lookup"><span data-stu-id="e37e8-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e37e8-116">Description</span><span class="sxs-lookup"><span data-stu-id="e37e8-116">Description</span></span></th>
<th><span data-ttu-id="e37e8-117">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="e37e8-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e37e8-118">URL du service de découverte automatique interne</span><span class="sxs-lookup"><span data-stu-id="e37e8-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e37e8-119">SAN = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e37e8-120">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="e37e8-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e37e8-121">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e37e8-122">Vous pouvez également utiliser le SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="e37e8-123">Conditions requises pour le certificat de pool frontal</span><span class="sxs-lookup"><span data-stu-id="e37e8-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e37e8-124">Description</span><span class="sxs-lookup"><span data-stu-id="e37e8-124">Description</span></span></th>
<th><span data-ttu-id="e37e8-125">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="e37e8-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e37e8-126">URL du service de découverte automatique interne</span><span class="sxs-lookup"><span data-stu-id="e37e8-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e37e8-127">SAN = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e37e8-128">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="e37e8-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e37e8-129">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e37e8-130">Vous pouvez également utiliser le SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="e37e8-131">Conditions requises pour les certificats de proxy inverse (AC publique)</span><span class="sxs-lookup"><span data-stu-id="e37e8-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e37e8-132">Description</span><span class="sxs-lookup"><span data-stu-id="e37e8-132">Description</span></span></th>
<th><span data-ttu-id="e37e8-133">Entrée de l’autre nom de l’objet</span><span class="sxs-lookup"><span data-stu-id="e37e8-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e37e8-134">URL du service de découverte automatique externe</span><span class="sxs-lookup"><span data-stu-id="e37e8-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="e37e8-135">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="e37e8-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="e37e8-136">Vous attribuez ce SAN au certificat attribué à l’écouteur SSL sur le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="e37e8-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="e37e8-137">Votre écouteur de proxy inverse aura des noms de remplacement pour vos URL de services Web externes (par exemple, SAN = lyncwebextpool01. contoso. com et dirwebexternal.contoso.com si vous avez déployé le réalisateur facultatif).</span><span class="sxs-lookup"><span data-stu-id="e37e8-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="e37e8-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e37e8-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

