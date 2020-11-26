---
title: 'Lync Server 2013 : Résumé des certificats - Directeur unique'
description: 'Résumé du certificat Lync Server 2013 : un seul directeur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cf930a73d9989ec44f52f1d70ee9e0f900e4d6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435193"
---
# <a name="certificate-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="afec6-103">Résumé des certificats - Directeur unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="afec6-103">Certificate summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afec6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afec6-104">

<span> </span></span></span>

<span data-ttu-id="afec6-105">_**Dernière modification de la rubrique :** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="afec6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="afec6-106">Les exigences en matière de certificat pour un seul directeur sont composées d’un certificat par défaut dont le nom du sujet comporte le nom de l’objet et des noms de remplacement pour les services que le directeur peut recevoir.</span><span class="sxs-lookup"><span data-stu-id="afec6-106">Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive.</span></span> <span data-ttu-id="afec6-107">Par ailleurs, il existe un certificat de jeton OAuth pour les besoins d’authentification de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="afec6-107">Additionally, there is an OAuth Token certificate for server to server authentication purposes.</span></span>

### <a name="certificates-for-director"></a><span data-ttu-id="afec6-108">Certificats pour Director</span><span class="sxs-lookup"><span data-stu-id="afec6-108">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afec6-109">Composant</span><span class="sxs-lookup"><span data-stu-id="afec6-109">Component</span></span></th>
<th><span data-ttu-id="afec6-110">Nom du sujet (SN)</span><span class="sxs-lookup"><span data-stu-id="afec6-110">Subject name (SN)</span></span></th>
<th><span data-ttu-id="afec6-111">Autres noms d’objet (SAN)</span><span class="sxs-lookup"><span data-stu-id="afec6-111">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="afec6-112">Commentaires</span><span class="sxs-lookup"><span data-stu-id="afec6-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afec6-113">Par défaut</span><span class="sxs-lookup"><span data-stu-id="afec6-113">Default</span></span></p></td>
<td><p><span data-ttu-id="afec6-114">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="afec6-114">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="afec6-115">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="afec6-115">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="afec6-116">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="afec6-116">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="afec6-117">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="afec6-117">meet.contoso.com</span></span></p>
<p><span data-ttu-id="afec6-118">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="afec6-118">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="afec6-119">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="afec6-119">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="afec6-120">(Facultatif) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="afec6-120">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="afec6-121">Les certificats de réalisateur peuvent être demandés auprès d’une autorité de certification (CA) gérée en interne ou auprès d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="afec6-121">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="afec6-122">Le directeur répond aux requêtes du proxy inverse dans le périmètre ou du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="afec6-122">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span> <span data-ttu-id="afec6-123">Les clients internes n’utiliseront pas le directeur.</span><span class="sxs-lookup"><span data-stu-id="afec6-123">Internal clients will not use the Director.</span></span></p>
<p><span data-ttu-id="afec6-124">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="afec6-124">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afec6-125">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="afec6-125">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="afec6-126">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="afec6-126">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="afec6-127">Aucune entrée</span><span class="sxs-lookup"><span data-stu-id="afec6-127">No Entry</span></span></p></td>
<td><div>

> [!IMPORTANT]  
> <span data-ttu-id="afec6-128">Notez que la longueur de la clé minimum est de 1024, mais vous pouvez recevoir un avertissement indiquant que la longueur de la clé minimum recommandée est 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="afec6-128">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


</div>
<p><span data-ttu-id="afec6-129">Le certificat OAuthTokenIssuer est un certificat à usage unique qui permet d’authentifier des serveurs dans un environnement à grande échelle et qui peut être demandé auprès d’une autorité de certification interne ou d’une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="afec6-129">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="afec6-130">Le certificat est requis.</span><span class="sxs-lookup"><span data-stu-id="afec6-130">The certificate is required.</span></span></p><span data-ttu-id="afec6-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afec6-131"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

