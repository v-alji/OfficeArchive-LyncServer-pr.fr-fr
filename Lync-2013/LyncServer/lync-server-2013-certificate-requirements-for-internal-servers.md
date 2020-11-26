---
title: 'Lync Server 2013 : Exigences de certificat pour les serveurs internes'
description: 'Lync Server 2013 : conditions de certificat requises pour les serveurs internes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435354"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="d33c3-103">Exigences de certificat pour les serveurs internes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d33c3-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d33c3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d33c3-104">

<span> </span></span></span>

<span data-ttu-id="d33c3-105">_**Dernière modification de la rubrique :** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="d33c3-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="d33c3-106">Les serveurs internes exécutant Lync Server et qui nécessitent des certificats incluent Standard Edition Server, Enterprise Edition front end Server, serveur de médiation et Director.</span><span class="sxs-lookup"><span data-stu-id="d33c3-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="d33c3-107">Le tableau suivant répertorie les conditions requises pour les certificats pour ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="d33c3-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="d33c3-108">Vous pouvez utiliser l’Assistant certificat de serveur Lync pour demander ces certificats.</span><span class="sxs-lookup"><span data-stu-id="d33c3-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="d33c3-109">Les certificats génériques sont pris en charge pour les noms de remplacement d’objet associés aux URL simples sur le pool frontal, serveur frontal ou Director.</span><span class="sxs-lookup"><span data-stu-id="d33c3-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="d33c3-110">Pour plus d’informations sur la prise en charge des certificats génériques, voir <A href="lync-server-2013-wildcard-certificate-support.md">prise en charge des certificats génériques dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d33c3-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="d33c3-111">Même si une autorité de certification d’entreprise interne est recommandée pour les serveurs internes, vous pouvez également utiliser une autorité de certification publique.</span><span class="sxs-lookup"><span data-stu-id="d33c3-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="d33c3-112">Pour obtenir une liste des autorités de certification publiques qui fournissent des certificats qui répondent à des exigences spécifiques pour les certificats de communications unifiées (UC) et qui ont un partenariat avec Microsoft pour s’assurer qu’ils fonctionnent avec l’Assistant certificat de Lync Server, voir l’article 929395 de la base de connaissances Microsoft, « partenaires de certification de communications unifiées » pour Exchange Server et pour Communications Server» [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="d33c3-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="d33c3-113">La communication avec d’autres applications et serveurs, comme Exchange 2013, nécessite un certificat pris en charge par les autres applications et produits.</span><span class="sxs-lookup"><span data-stu-id="d33c3-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="d33c3-114">Pour la version 2013, Lync Server 2013 et d’autres produits Microsoft Server, dont Exchange 2013 et SharePoint Server, prennent en charge le protocole d’autorisation Open (OAuth) pour l’authentification et l’autorisation de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="d33c3-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="d33c3-115">Pour plus d’informations, reportez-vous à la section [gestion des applications d’authentification de serveur à serveur (OAuth) et de partenariat dans Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) dans la documentation de déploiement ou la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="d33c3-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="d33c3-116">Pour les connexions provenant de clients exécutant le système d’exploitation Windows 7, le système d’exploitation Windows Server 2008, le système d’exploitation Windows Server 2008 R2, le système d’exploitation Windows Vista et Microsoft Lync Phone Edition, Lync Server 2013 inclut la prise en charge des certificats de la fonction de hachage cryptographique SHA-256.</span><span class="sxs-lookup"><span data-stu-id="d33c3-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="d33c3-117">Pour prendre en charge l’accès externe à l’aide de l’algorithme SHA-256, le certificat externe est émis par une autorité de certification publique utilisant SHA-256.</span><span class="sxs-lookup"><span data-stu-id="d33c3-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="d33c3-118">Les tableaux suivants illustrent les exigences de certificat par rôle de serveur pour les pools frontaux et les serveurs Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d33c3-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="d33c3-119">Il s’agit d’un certificat de serveur Web standard, d’une clé privée, d’un serveur non transférable.</span><span class="sxs-lookup"><span data-stu-id="d33c3-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="d33c3-120">Notez que l’utilisation améliorée de la clé du serveur est automatiquement configurée lorsque vous utilisez l’Assistant Certificat pour demander des certificats.</span><span class="sxs-lookup"><span data-stu-id="d33c3-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d33c3-121">Chaque nom convivial de certificat doit être unique dans le magasin d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="d33c3-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="d33c3-122">Si vous avez configuré sipinternal.contoso.com ou sipexternal.contoso.com dans votre DNS, vous devez l’ajouter dans le nom de l’autre nom de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="d33c3-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="d33c3-123">Certificats pour Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="d33c3-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33c3-124">Certificat</span><span class="sxs-lookup"><span data-stu-id="d33c3-124">Certificate</span></span></th>
<th><span data-ttu-id="d33c3-125">Nom de l’objet/nom usuel</span><span class="sxs-lookup"><span data-stu-id="d33c3-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d33c3-126">Autre nom du sujet</span><span class="sxs-lookup"><span data-stu-id="d33c3-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="d33c3-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="d33c3-127">Example</span></span></th>
<th><span data-ttu-id="d33c3-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d33c3-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-129">Par défaut</span><span class="sxs-lookup"><span data-stu-id="d33c3-129">Default</span></span></p></td>
<td><p><span data-ttu-id="d33c3-130">Nom de domaine complet (FQDN) du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-131">Nom de domaine complet (FQDN) du pool et nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="d33c3-132">Si vous disposez de plusieurs domaines SIP et avez activé la configuration automatique des clients, l’Assistant Certificat détecte et ajoute le nom complet de chaque domaine SIP pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d33c3-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="d33c3-133">Si ce pool est le serveur d’ouverture de session automatique pour les clients et si la correspondance DNS (Domain Name System) stricte est requise dans la stratégie de groupe, vous avez également besoin d’entrées pour sip.sipdomain (pour chacun des domaines SIP dont vous disposez).</span><span class="sxs-lookup"><span data-stu-id="d33c3-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d33c3-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-135">Si ce pool est le serveur d’ouverture de session automatique pour les clients et si la correspondance DNS stricte est requise dans la stratégie de groupe, SAN=sip.contoso.com et SAN=sip.fabrikam.com sont également nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d33c3-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-136">Sur un serveur Standard Edition Server, le nom de domaine complet du serveur est identique au nom de domaine complet du pool.</span><span class="sxs-lookup"><span data-stu-id="d33c3-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="d33c3-137">L’Assistant détecte les domaines SIP indiqués lors de l’installation et les ajoute automatiquement à l’autre nom du sujet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="d33c3-138">Vous pouvez aussi utiliser ce certificat pour l’authentification de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="d33c3-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d33c3-139">Web interne</span><span class="sxs-lookup"><span data-stu-id="d33c3-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="d33c3-140">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d33c3-141">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-142">Nom de domaine complet web interne (qui est le même que celui du serveur)</span><span class="sxs-lookup"><span data-stu-id="d33c3-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d33c3-143">URL simples Meet</span><span class="sxs-lookup"><span data-stu-id="d33c3-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d33c3-144">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-145">URL simple Admin</span><span class="sxs-lookup"><span data-stu-id="d33c3-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-146">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-148">Utilisation d’un certificat de caractère générique :</span><span class="sxs-lookup"><span data-stu-id="d33c3-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d33c3-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-150">Vous ne pouvez pas remplacer le FQDN Web interne dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="d33c3-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="d33c3-151">Si vous avez plusieurs URL de la réunion, vous devez les inclure en tant qu’autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d33c3-152">Les entrées de caractères génériques sont prises en charge pour les entrées d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="d33c3-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-153">Web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="d33c3-154">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d33c3-155">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-156">Nom de domaine complet web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-157">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-158">URL simples de réunion par domaine SIP</span><span class="sxs-lookup"><span data-stu-id="d33c3-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="d33c3-159">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-161">Utilisation d’un certificat de caractère générique :</span><span class="sxs-lookup"><span data-stu-id="d33c3-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d33c3-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-163">Si vous avez plusieurs URL de la réunion, vous devez les inclure en tant qu’autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d33c3-164">Les entrées de caractères génériques sont prises en charge pour les entrées d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="d33c3-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="d33c3-165">Certificats pour serveur frontal dans un pool frontal</span><span class="sxs-lookup"><span data-stu-id="d33c3-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33c3-166">Certificat</span><span class="sxs-lookup"><span data-stu-id="d33c3-166">Certificate</span></span></th>
<th><span data-ttu-id="d33c3-167">Nom de l’objet/nom usuel</span><span class="sxs-lookup"><span data-stu-id="d33c3-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d33c3-168">Autre nom du sujet</span><span class="sxs-lookup"><span data-stu-id="d33c3-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="d33c3-169">Exemple</span><span class="sxs-lookup"><span data-stu-id="d33c3-169">Example</span></span></th>
<th><span data-ttu-id="d33c3-170">Commentaires</span><span class="sxs-lookup"><span data-stu-id="d33c3-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-171">Par défaut</span><span class="sxs-lookup"><span data-stu-id="d33c3-171">Default</span></span></p></td>
<td><p><span data-ttu-id="d33c3-172">Nom de domaine complet du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-173">Nom de domaine complet (FQDN) du pool et du nom de domaine complet du serveur.</span><span class="sxs-lookup"><span data-stu-id="d33c3-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="d33c3-174">Si vous disposez de plusieurs domaines SIP et avez activé la configuration automatique des clients, l’Assistant Certificat détecte et ajoute le nom complet de chaque domaine SIP pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d33c3-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="d33c3-175">Si ce pool est le serveur de connexion automatique pour les clients et si la correspondance DNS stricte est requise dans la stratégie de groupe, vous avez également besoin d’entrées pour SIP. sipdomain (pour chaque domaine SIP que vous utilisez).</span><span class="sxs-lookup"><span data-stu-id="d33c3-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d33c3-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com </span><span class="sxs-lookup"><span data-stu-id="d33c3-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-177">Si ce pool est le serveur d’ouverture de session automatique pour les clients et si la correspondance DNS stricte est requise dans la stratégie de groupe, SAN=sip.contoso.com et SAN=sip.fabrikam.com sont également nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d33c3-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-178">L’Assistant détecte les domaines SIP indiqués lors de l’installation et les ajoute automatiquement à l’autre nom du sujet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="d33c3-179">Vous pouvez aussi utiliser ce certificat pour l’authentification de serveur à serveur.</span><span class="sxs-lookup"><span data-stu-id="d33c3-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d33c3-180">Site Web interne</span><span class="sxs-lookup"><span data-stu-id="d33c3-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="d33c3-181">Nom de domaine complet du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-182">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-183">Nom de domaine complet web interne (qui N’EST PAS le même que celui du serveur)</span><span class="sxs-lookup"><span data-stu-id="d33c3-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d33c3-184">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-185">Nom de domaine complet du pool Lync</span><span class="sxs-lookup"><span data-stu-id="d33c3-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-186">URL simples Meet</span><span class="sxs-lookup"><span data-stu-id="d33c3-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d33c3-187">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-188">URL simple Admin</span><span class="sxs-lookup"><span data-stu-id="d33c3-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-189">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-191">Utilisation d’un certificat de caractère générique :</span><span class="sxs-lookup"><span data-stu-id="d33c3-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d33c3-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-193">Si vous avez plusieurs URL de la réunion, vous devez les inclure en tant qu’autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d33c3-194">Les entrées de caractères génériques sont prises en charge pour les entrées d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="d33c3-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-195">Web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="d33c3-196">Nom de domaine complet du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-197">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-198">Nom de domaine complet web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-199">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-200">URL simple Admin</span><span class="sxs-lookup"><span data-stu-id="d33c3-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-201">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-203">Utilisation d’un certificat de caractère générique :</span><span class="sxs-lookup"><span data-stu-id="d33c3-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d33c3-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d33c3-205">Si vous avez plusieurs URL de la réunion, vous devez les inclure en tant qu’autres noms d’objet.</span><span class="sxs-lookup"><span data-stu-id="d33c3-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d33c3-206">Les entrées de caractères génériques sont prises en charge pour les entrées d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="d33c3-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="d33c3-207">Certificats pour Director</span><span class="sxs-lookup"><span data-stu-id="d33c3-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33c3-208">Certificat</span><span class="sxs-lookup"><span data-stu-id="d33c3-208">Certificate</span></span></th>
<th><span data-ttu-id="d33c3-209">Nom de l’objet/nom usuel</span><span class="sxs-lookup"><span data-stu-id="d33c3-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d33c3-210">Autre nom du sujet</span><span class="sxs-lookup"><span data-stu-id="d33c3-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="d33c3-211">Exemple</span><span class="sxs-lookup"><span data-stu-id="d33c3-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-212">Par défaut</span><span class="sxs-lookup"><span data-stu-id="d33c3-212">Default</span></span></p></td>
<td><p><span data-ttu-id="d33c3-213">Nom de domaine complet (FQDN) du pool de réalisateurs</span><span class="sxs-lookup"><span data-stu-id="d33c3-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-214">Nom de domaine complet (FQDN) du réalisateur du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="d33c3-215">Si ce pool est le serveur de connexion automatique pour les clients et si la correspondance DNS stricte est requise dans la stratégie de groupe, vous avez également besoin d’entrées pour SIP. sipdomain (pour chaque domaine SIP que vous utilisez).</span><span class="sxs-lookup"><span data-stu-id="d33c3-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d33c3-216">SN = dir-pool.contoso.com ; SAN = dir-pool.contoso.com ; SAN = DIR01. contoso. com</span><span class="sxs-lookup"><span data-stu-id="d33c3-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-217">Si ce pool de directeurs est le serveur de connexion automatique pour les clients et si la correspondance DNS stricte est requise dans la stratégie de groupe, vous devez également disposer de SAN = SIP. contoso. com ; SAN = SIP. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="d33c3-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d33c3-218">Site Web interne</span><span class="sxs-lookup"><span data-stu-id="d33c3-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="d33c3-219">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d33c3-220">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-221">Nom de domaine complet web interne (qui est le même que celui du serveur)</span><span class="sxs-lookup"><span data-stu-id="d33c3-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d33c3-222">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-223">Nom de domaine complet du pool Lync</span><span class="sxs-lookup"><span data-stu-id="d33c3-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-224">URL simples Meet</span><span class="sxs-lookup"><span data-stu-id="d33c3-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d33c3-225">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-226">URL simple Admin</span><span class="sxs-lookup"><span data-stu-id="d33c3-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-227">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-230">Web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="d33c3-231">Nom de domaine complet du serveur</span><span class="sxs-lookup"><span data-stu-id="d33c3-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d33c3-232">Pour chaque élément suivant :</span><span class="sxs-lookup"><span data-stu-id="d33c3-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d33c3-233">Nom de domaine complet web externe</span><span class="sxs-lookup"><span data-stu-id="d33c3-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d33c3-234">URL simple Dial-in</span><span class="sxs-lookup"><span data-stu-id="d33c3-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-235">URL simple Admin</span><span class="sxs-lookup"><span data-stu-id="d33c3-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d33c3-236">Ou une entrée de caractère générique pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="d33c3-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d33c3-237">Le FQDN Web de Director doit être différent du serveur frontal ou du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="d33c3-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="d33c3-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d33c3-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d33c3-240">Si vous disposez d’un pool de serveurs de médiation autonome, vous avez besoin des certificats répertoriés dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d33c3-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="d33c3-241">Si vous collocate un serveur de médiation avec les serveurs frontaux, les certificats répertoriés dans le tableau « certificats pour le serveur frontal du pool frontal », plus haut dans cette rubrique sont suffisants.</span><span class="sxs-lookup"><span data-stu-id="d33c3-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="d33c3-242">Certificats pour un serveur de médiation autonome</span><span class="sxs-lookup"><span data-stu-id="d33c3-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33c3-243">Certificat</span><span class="sxs-lookup"><span data-stu-id="d33c3-243">Certificate</span></span></th>
<th><span data-ttu-id="d33c3-244">Nom de l’objet/nom usuel</span><span class="sxs-lookup"><span data-stu-id="d33c3-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d33c3-245">Autre nom du sujet</span><span class="sxs-lookup"><span data-stu-id="d33c3-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="d33c3-246">Exemple</span><span class="sxs-lookup"><span data-stu-id="d33c3-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-247">Par défaut</span><span class="sxs-lookup"><span data-stu-id="d33c3-247">Default</span></span></p></td>
<td><p><span data-ttu-id="d33c3-248">Nom de domaine complet du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d33c3-249">Nom de domaine complet du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="d33c3-250">Nom de domaine complet du serveur de membres du pool</span><span class="sxs-lookup"><span data-stu-id="d33c3-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="d33c3-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d33c3-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="d33c3-252">Certificats pour l’appareil de branchement survivant</span><span class="sxs-lookup"><span data-stu-id="d33c3-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d33c3-253">Certificat</span><span class="sxs-lookup"><span data-stu-id="d33c3-253">Certificate</span></span></th>
<th><span data-ttu-id="d33c3-254">Nom de l’objet/nom usuel</span><span class="sxs-lookup"><span data-stu-id="d33c3-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d33c3-255">Autre nom du sujet</span><span class="sxs-lookup"><span data-stu-id="d33c3-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="d33c3-256">Exemple</span><span class="sxs-lookup"><span data-stu-id="d33c3-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d33c3-257">Par défaut</span><span class="sxs-lookup"><span data-stu-id="d33c3-257">Default</span></span></p></td>
<td><p><span data-ttu-id="d33c3-258">Nom de domaine complet de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d33c3-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="d33c3-259">SIP. &lt; sipdomain &gt; (nécessite une entrée par domaine SIP)</span><span class="sxs-lookup"><span data-stu-id="d33c3-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="d33c3-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d33c3-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="d33c3-261">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d33c3-261">See Also</span></span>


[<span data-ttu-id="d33c3-262">Prise en charge des certificats comportant des caractères génériques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d33c3-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="d33c3-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d33c3-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

