---
title: 'Lync Server 2013 : Résumé des certificats - Équilibrage de charge DNS et matérielle'
description: 'Rapport de synthèse des certificats de Lync Server 2013 : DNS et HLB.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - DNS and HLB load balanced
ms:assetid: 8318a1a4-b423-47b7-95e6-9541adfad391
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205047(v=OCS.15)
ms:contentKeyID: 48184676
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 97a89975af16b6e39625677f787d3726f00c76c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435319"
---
# <a name="certificate-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="45052-103">Résumé des certificats - Équilibrage de charge DNS et matérielle dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45052-103">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45052-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45052-104">

<span> </span></span></span>

<span data-ttu-id="45052-105">_**Dernière modification de la rubrique :** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="45052-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="45052-106">Les exigences en matière de certificat pour un directeur avec l’équilibrage de charge DNS et un équilibreur de charge matérielle utilise un certificat par défaut qui comporte un nom de sujet et des noms de remplacement d’objet pour les services que le directeur peut recevoir.</span><span class="sxs-lookup"><span data-stu-id="45052-106">Certificate requirements for a Director with DNS load balancing and a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="45052-107">Un certificat est demandé pour chaque réalisateur du pool.</span><span class="sxs-lookup"><span data-stu-id="45052-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="45052-108">Il est important de se souvenir que le service d’équilibrage de la charge matérielle ne charge que le trafic du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="45052-108">It is important to remember that the hardware load balancer is load balancing only the traffic from the reverse proxy.</span></span> <span data-ttu-id="45052-109">Par ailleurs, il existe un certificat de jeton OAuth pour les rôles d’authentification de serveur à serveur qui est installé sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="45052-109">Additionally, there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="45052-110">Certificats pour Director</span><span class="sxs-lookup"><span data-stu-id="45052-110">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45052-111">Composant</span><span class="sxs-lookup"><span data-stu-id="45052-111">Component</span></span></th>
<th><span data-ttu-id="45052-112">Nom du sujet (SN)</span><span class="sxs-lookup"><span data-stu-id="45052-112">Subject name (SN)</span></span></th>
<th><span data-ttu-id="45052-113">Autres noms d’objet (SAN)</span><span class="sxs-lookup"><span data-stu-id="45052-113">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="45052-114">Commentaires</span><span class="sxs-lookup"><span data-stu-id="45052-114">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45052-115">Par défaut</span><span class="sxs-lookup"><span data-stu-id="45052-115">Default</span></span></p></td>
<td><p><span data-ttu-id="45052-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="45052-116">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="45052-117">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="45052-117">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="45052-118">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="45052-118">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="45052-119">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="45052-119">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="45052-120">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="45052-120">meet.contoso.com</span></span></p>
<p><span data-ttu-id="45052-121">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="45052-121">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="45052-122">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="45052-122">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="45052-123">(Facultatif) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="45052-123">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="45052-124">Les certificats de réalisateur peuvent être demandés auprès d’une autorité de certification (CA) gérée en interne ou auprès d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="45052-124">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="45052-125">Le directeur répond aux requêtes du proxy inverse dans le périmètre ou du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="45052-125">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="45052-126">Les clients internes n’utiliseront pas le directeur.</span><span class="sxs-lookup"><span data-stu-id="45052-126">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="45052-127">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="45052-127">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45052-128">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="45052-128">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="45052-129">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="45052-129">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="45052-130">Aucune entrée</span><span class="sxs-lookup"><span data-stu-id="45052-130">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="45052-131">Notez que la longueur de la clé minimum est de 1024, mais vous pouvez recevoir un avertissement indiquant que la longueur de la clé minimum recommandée est 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="45052-131">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="45052-132">Le certificat OAuthTokenIssuer est un certificat à usage unique qui permet d’authentifier des serveurs dans un environnement à grande échelle et qui peut être demandé auprès d’une autorité de certification interne ou d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="45052-132">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="45052-133">Le certificat est requis.</span><span class="sxs-lookup"><span data-stu-id="45052-133">The certificate is required.</span></span></p><span data-ttu-id="45052-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45052-134"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

