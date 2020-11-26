---
title: 'Lync Server 2013 : chiffrement'
description: 'Lync Server 2013 : chiffrement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Encryption for Lync Server 2013
ms:assetid: d18c74a6-385b-407b-98eb-0d525fa38fea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481135(v=OCS.15)
ms:contentKeyID: 59893874
ms.date: 09/14/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ab2c46af16cfdbb9a01631777e65219acb2ceb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428719"
---
# <a name="encryption-for-lync-server-2013"></a><span data-ttu-id="49385-103">Chiffrement pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49385-103">Encryption for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49385-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49385-104">

<span> </span></span></span>

<span data-ttu-id="49385-105">_**Dernière modification de la rubrique :** 2017-09-14_</span><span class="sxs-lookup"><span data-stu-id="49385-105">_**Topic Last Modified:** 2017-09-14_</span></span>

<span data-ttu-id="49385-106">Microsoft Lync Server 2013 utilise TLS et MTLS pour chiffrer les messages instantanés.</span><span class="sxs-lookup"><span data-stu-id="49385-106">Microsoft Lync Server 2013 uses TLS and MTLS to encrypt instant messages.</span></span> <span data-ttu-id="49385-107">Tout le trafic de serveur à serveur requiert MTLS, que le trafic soit confiné au réseau interne ou qu’il traverse le périmètre réseau interne.</span><span class="sxs-lookup"><span data-stu-id="49385-107">All server-to-server traffic requires MTLS, regardless of whether the traffic is confined to the internal network or crosses the internal network perimeter.</span></span> <span data-ttu-id="49385-108">TLS est facultatif, mais fortement recommandé entre le serveur de médiation et la passerelle multimédia.</span><span class="sxs-lookup"><span data-stu-id="49385-108">TLS is optional but strongly recommended between the Mediation Server and media gateway.</span></span> <span data-ttu-id="49385-109">Si TLS est configuré sur cette liaison, MTLS est requis.</span><span class="sxs-lookup"><span data-stu-id="49385-109">If TLS is configured on this link, MTLS is required.</span></span> <span data-ttu-id="49385-110">Par conséquent, la passerelle doit être configurée avec un certificat provenant d’une autorité de certification approuvée par le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="49385-110">Therefore, the gateway must be configured with a certificate from a CA that is trusted by the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49385-111">Un avis de sécurité relatif à SSL 3.0 a été publié en 2014.</span><span class="sxs-lookup"><span data-stu-id="49385-111">A security advisory regarding SSL 3.0 was published in 2014.</span></span> <span data-ttu-id="49385-112">La désactivation de SSL 3,0 dans Lync Server 2013 est une option prise en charge.</span><span class="sxs-lookup"><span data-stu-id="49385-112">Disabling SSL 3.0 in Lync Server 2013 is a supported option.</span></span> <span data-ttu-id="49385-113">Pour en savoir plus sur l’avis de sécurité, voir <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A> .</span><span class="sxs-lookup"><span data-stu-id="49385-113">To learn more about the security advisory, see <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A>.</span></span>



</div>

<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="sûreté" alt="security" /><span data-ttu-id="49385-115">Note de sécurité :</span><span class="sxs-lookup"><span data-stu-id="49385-115">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49385-116">Pour vous assurer que le protocole cryptographique le plus puissant est utilisé, Lync Server 2013 propose des protocoles de chiffrement TLS dans l’ordre suivant pour les clients : <strong>tls 1,2</strong> , <strong>TLS 1,1</strong>, <strong>TLS 1,0</strong>.</span><span class="sxs-lookup"><span data-stu-id="49385-116">To ensure the strongest cryptographic protocol is used, Lync Server 2013 will offer TLS encryption protocols in the following order to clients: <strong>TLS 1.2</strong> , <strong>TLS 1.1</strong>, <strong>TLS 1.0</strong>.</span></span> <span data-ttu-id="49385-117">Le protocole TLS est un aspect essentiel de Lync Server 2013 et donc requis pour gérer un environnement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="49385-117">TLS is a critical aspect of Lync Server 2013 and thus it is required in order to maintain a supported environment.</span></span></td>
</tr>
</tbody>
</table>


</div>

<span data-ttu-id="49385-118">La configuration requise pour le trafic client à client varie selon que le trafic traverse le pare-feu interne de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="49385-118">Requirements for client-to-client traffic depend on whether that traffic crosses the internal corporate firewall.</span></span> <span data-ttu-id="49385-119">Le trafic interne strictement disponible peut utiliser la valeur TLS, auquel cas le message instantané est crypté, et ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="49385-119">Strictly internal traffic can use either TLS, in which case the instant message is encrypted, or TCP, in which case it is not.</span></span>

<span data-ttu-id="49385-120">Le tableau suivant résume les exigences de protocole pour chaque type de trafic.</span><span class="sxs-lookup"><span data-stu-id="49385-120">The following table summarizes the protocol requirements for each type of traffic.</span></span>

### <a name="traffic-protection"></a><span data-ttu-id="49385-121">Protection du trafic</span><span class="sxs-lookup"><span data-stu-id="49385-121">Traffic Protection</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49385-122">Type de trafic</span><span class="sxs-lookup"><span data-stu-id="49385-122">Traffic type</span></span></th>
<th><span data-ttu-id="49385-123">Protégé par</span><span class="sxs-lookup"><span data-stu-id="49385-123">Protected by</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49385-124">Serveur à serveur</span><span class="sxs-lookup"><span data-stu-id="49385-124">Server-to-server</span></span></p></td>
<td><p><span data-ttu-id="49385-125">MTLS</span><span class="sxs-lookup"><span data-stu-id="49385-125">MTLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49385-126">Client à serveur</span><span class="sxs-lookup"><span data-stu-id="49385-126">Client-to-server</span></span></p></td>
<td><p><span data-ttu-id="49385-127">TLS</span><span class="sxs-lookup"><span data-stu-id="49385-127">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49385-128">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="49385-128">Instant messaging and presence</span></span></p></td>
<td><p><span data-ttu-id="49385-129">TLS (si TLS est configuré)</span><span class="sxs-lookup"><span data-stu-id="49385-129">TLS (if configured for TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49385-130">Partage multimédia audio, vidéo et de bureau</span><span class="sxs-lookup"><span data-stu-id="49385-130">Audio and video and desktop sharing of media</span></span></p></td>
<td><p><span data-ttu-id="49385-131">SRTP</span><span class="sxs-lookup"><span data-stu-id="49385-131">SRTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49385-132">Partage du bureau (signalisation)</span><span class="sxs-lookup"><span data-stu-id="49385-132">Desktop sharing (signaling)</span></span></p></td>
<td><p><span data-ttu-id="49385-133">TLS</span><span class="sxs-lookup"><span data-stu-id="49385-133">TLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49385-134">Conférence web</span><span class="sxs-lookup"><span data-stu-id="49385-134">Web conferencing</span></span></p></td>
<td><p><span data-ttu-id="49385-135">TLS</span><span class="sxs-lookup"><span data-stu-id="49385-135">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49385-136">Téléchargement de contenu de réunion, téléchargement de carnet d’adresses, développement de groupe de distribution</span><span class="sxs-lookup"><span data-stu-id="49385-136">Meeting content download, address book download, distribution group expansion</span></span></p></td>
<td><p><span data-ttu-id="49385-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="49385-137">HTTPS</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="media-encryption"></a><span data-ttu-id="49385-138">Chiffrement multimédia</span><span class="sxs-lookup"><span data-stu-id="49385-138">Media Encryption</span></span>

<span data-ttu-id="49385-139">Le trafic multimédia est chiffré à l'aide du protocole SRTP (Secure Real-time Transport Protocol), un profil du protocole RTP (Real-Time Transport Protocol) qui offre confidentialité, authentification et protection contre les attaques sur le trafic RTP.</span><span class="sxs-lookup"><span data-stu-id="49385-139">Media traffic is encrypted using Secure RTP (SRTP), a profile of Real-Time Transport Protocol (RTP) that provides confidentiality, authentication, and replay attack protection to RTP traffic.</span></span> <span data-ttu-id="49385-140">De plus, les données multimédias acheminées dans les deux directions entre le serveur de médiation et son tronçon suivant interne sont également chiffrées avec SRTP.</span><span class="sxs-lookup"><span data-stu-id="49385-140">In addition, media flowing in both directions between the Mediation Server and its internal next hop is also encrypted using SRTP.</span></span> <span data-ttu-id="49385-141">Par défaut, le flux multimédia dans les deux directions entre le serveur de médiation et une passerelle multimédia n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="49385-141">Media flowing in both directions between the Mediation Server and a media gateway is not encrypted by default.</span></span> <span data-ttu-id="49385-142">Le serveur de médiation peut prendre en charge le chiffrement sur la passerelle multimédia, mais la passerelle doit prendre en charge MTLS et le stockage d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="49385-142">The Mediation Server can support encryption to the media gateway, but the gateway must support MTLS and storage of a certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49385-143">L’audio/vidéo (A/V) est pris en charge avec la nouvelle version de Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="49385-143">Audio/Video (A/V) is supported with the new version of Windows Live Messenger.</span></span> <span data-ttu-id="49385-144">Si vous implémentez une fédération A/V avec Windows Live Messenger, vous devez également modifier le niveau de chiffrement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="49385-144">If you are implementing A/V federation with Windows Live Messenger, you must also modify the Lync Server encryption level.</span></span> <span data-ttu-id="49385-145">Par défaut, ce paramètre est défini sur Requis.</span><span class="sxs-lookup"><span data-stu-id="49385-145">By default, the encryption level is Required.</span></span> <span data-ttu-id="49385-146">Vous devez définir ce paramètre sur pris en charge à l’aide de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="49385-146">You must change this setting to Supported by using the Lync Server Management Shell.</span></span> <span data-ttu-id="49385-147">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-deploying-external-user-access.md">déploiement d’un accès utilisateur externe dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="49385-147">For more information, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="49385-148">Le trafic des contenus multimédias audio et vidéo n’est pas crypté entre les clients Microsoft Lync 2013 et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="49385-148">Audio and video media traffic is not encrypted between Microsoft Lync 2013 and Windows Live clients.</span></span>

</div>

<div>

## <a name="fips"></a><span data-ttu-id="49385-149">FIPS</span><span class="sxs-lookup"><span data-stu-id="49385-149">FIPS</span></span>

<span data-ttu-id="49385-150">Lync Server 2013 et Microsoft Exchange Server 2013 prennent en charge les algorithmes 140-2 FIPS (Federal Information Processing Standard), si les systèmes d’exploitation Windows Server sont configurés pour utiliser les algorithmes 140-2 FIPS FIPS pour le chiffrement du système.</span><span class="sxs-lookup"><span data-stu-id="49385-150">Lync Server 2013 and Microsoft Exchange Server 2013 operate with support for Federal Information Processing Standard (FIPS) 140-2 algorithms if the Windows Server operating systems are configured to use the FIPS 140-2 algorithms for system cryptography.</span></span> <span data-ttu-id="49385-151">Pour mettre en œuvre la prise en charge du FIPS, vous devez configurer chaque serveur exécutant Lync Server 2013 pour le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="49385-151">To implement FIPS support, you must configure each server running Lync Server 2013 to support it.</span></span> <span data-ttu-id="49385-152">Pour plus d’informations sur l’utilisation des algorithmes compatibles FIPS et sur l’implémentation de la prise en charge du FIPS, voir l’article 811833 de la base de connaissances Microsoft, effets de l’activation du paramètre de sécurité « chiffrement de système : utiliser les algorithmes compatibles FIPS pour le chiffrement, le hachage et la signature » dans Windows XP et les versions ultérieures de Windows [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833) .</span><span class="sxs-lookup"><span data-stu-id="49385-152">For details about the use of FIPS-compliant algorithms and how to implement FIPS support, see Microsoft Knowledge Base article 811833, The effects of enabling the “System cryptography: Use FIPS compliant algorithms for encryption, hashing, and signing" security setting in Windows XP and in later versions of Windows at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833).</span></span> <span data-ttu-id="49385-153">Pour plus d’informations sur la prise en charge et les limitations de FIPS 140-2 dans Exchange 2010, voir Exchange 2010 SP1 et prise en charge des algorithmes compatibles FIPS à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335) .</span><span class="sxs-lookup"><span data-stu-id="49385-153">For details about FIPS 140-2 support and limitations in Exchange 2010, see Exchange 2010 SP1 and Support for FIPS Compliant Algorithms at [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335).</span></span>

<span data-ttu-id="49385-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49385-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

