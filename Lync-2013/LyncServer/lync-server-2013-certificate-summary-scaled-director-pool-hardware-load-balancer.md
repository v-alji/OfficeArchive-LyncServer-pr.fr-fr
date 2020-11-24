---
title: Résumé des certificats - Pool directeur mis à l’échelle, équilibreur de charge matérielle
description: Résumé de certification-pool de Directors mis à l’échelle, équilibrage de charge matérielle.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394801"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="f5f79-103">Résumé des certificats - Pool directeur mis à l’échelle, équilibreur de charge matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5f79-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5f79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5f79-104">

<span> </span></span></span>

<span data-ttu-id="f5f79-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="f5f79-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="f5f79-106">Les exigences en matière de certificat pour un directeur avec un dispositif d’équilibrage de la charge matérielle utiliseront un certificat par défaut dont le nom du sujet comporte le nom de l’objet et des noms de remplacement pour les services que le pool de réalisateur peut recevoir.</span><span class="sxs-lookup"><span data-stu-id="f5f79-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="f5f79-107">Un certificat est demandé pour chaque réalisateur du pool.</span><span class="sxs-lookup"><span data-stu-id="f5f79-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="f5f79-108">De plus, il existe un certificat de jeton OAuth pour les rôles d’authentification de serveur à serveur qui est installé sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="f5f79-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="f5f79-109">Certificats pour un directeur mis à l’échelle à l’aide d’un équilibreur de charge matérielle</span><span class="sxs-lookup"><span data-stu-id="f5f79-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5f79-110">Composant</span><span class="sxs-lookup"><span data-stu-id="f5f79-110">Component</span></span></th>
<th><span data-ttu-id="f5f79-111">Nom du sujet (SN)</span><span class="sxs-lookup"><span data-stu-id="f5f79-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="f5f79-112">Autres noms d’objet (SAN)</span><span class="sxs-lookup"><span data-stu-id="f5f79-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="f5f79-113">Commentaires</span><span class="sxs-lookup"><span data-stu-id="f5f79-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5f79-114">Par défaut</span><span class="sxs-lookup"><span data-stu-id="f5f79-114">Default</span></span></p></td>
<td><p><span data-ttu-id="f5f79-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f5f79-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="f5f79-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f5f79-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="f5f79-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f5f79-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="f5f79-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5f79-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="f5f79-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5f79-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="f5f79-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5f79-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="f5f79-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5f79-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="f5f79-122">(Facultatif) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5f79-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f5f79-123">Les certificats de réalisateur peuvent être demandés auprès d’une autorité de certification (CA) gérée en interne ou auprès d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="f5f79-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="f5f79-124">Le directeur répond aux requêtes du proxy inverse dans le périmètre ou du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="f5f79-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="f5f79-125">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="f5f79-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5f79-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="f5f79-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="f5f79-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f5f79-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="f5f79-128">Aucune entrée</span><span class="sxs-lookup"><span data-stu-id="f5f79-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="f5f79-129">Notez que la longueur de la clé minimum est de 1024, mais vous pouvez recevoir un avertissement indiquant que la longueur de la clé minimum recommandée est 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="f5f79-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="f5f79-130">Le certificat OAuthTokenIssuer est un certificat à usage unique qui permet d’authentifier des serveurs dans un environnement à grande échelle et qui peut être demandé auprès d’une autorité de certification interne ou d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="f5f79-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="f5f79-131">Le certificat est requis.</span><span class="sxs-lookup"><span data-stu-id="f5f79-131">The certificate is required.</span></span></p><span data-ttu-id="f5f79-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5f79-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

