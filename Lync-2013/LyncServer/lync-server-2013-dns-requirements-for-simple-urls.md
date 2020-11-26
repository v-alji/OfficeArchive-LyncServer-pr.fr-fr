---
title: 'Lync Server 2013 : Enregistrements DNS requis pour les URL simples'
description: 'Lync Server 2013 : configuration requise pour DNS pour les URL simples.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for simple URLs
ms:assetid: 3a3c9b22-892f-45a7-b05c-539d358a1a86
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425874(v=OCS.15)
ms:contentKeyID: 48183912
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 84cc893fc06e9c57dcad6506d692b4484827b56a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437757"
---
# <a name="dns-requirements-for-simple-urls-in-lync-server-2013"></a><span data-ttu-id="5288c-103">Enregistrements DNS requis pour les URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5288c-103">DNS requirements for simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="https://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5288c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5288c-104">

<span> </span></span></span>

<span data-ttu-id="5288c-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="5288c-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="5288c-106">Lync Server 2013 prend en charge des URL simples qui simplifient la participation à des réunions pour vos utilisateurs et permettent d’accéder plus facilement aux outils d’administration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5288c-106">Lync Server 2013 supports simple URLs, which make joining meetings easier for your users, and make getting to Lync Server administrative tools easier for your administrators.</span></span> <span data-ttu-id="5288c-107">Pour plus d’informations sur les URL simples, voir [planification d’URL simples dans Lync Server 2013](lync-server-2013-planning-for-simple-urls.md).</span><span class="sxs-lookup"><span data-stu-id="5288c-107">For details about simple URLs, see [Planning for simple URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md).</span></span>

<span data-ttu-id="5288c-108">Lync Server prend en charge les trois URL simples suivantes : réunion, accès et administration. Vous devez configurer des URL simples pour la réunion et le rendez-vous, et l’URL simple d’administration est facultative.</span><span class="sxs-lookup"><span data-stu-id="5288c-108">Lync Server supports the following three simple URLs: Meet, Dial-In, and Admin. You are required to set up simple URLs for Meet and Dial-In, and the Admin simple URL is optional.</span></span> <span data-ttu-id="5288c-109">Les enregistrements DNS (Domain Name System) nécessaires à la prise en charge d’URL simples dépendent de la façon dont vous avez défini ces URL simples et de la prise en charge de la reprise après sinistre pour des URL simples.</span><span class="sxs-lookup"><span data-stu-id="5288c-109">The Domain Name System (DNS) records that you need to support simple URLs depend on how you have defined these simple URLs, and whether you want to support disaster recovery for Simple URLs.</span></span>

<div>

## <a name="simple-url-option-1"></a><span data-ttu-id="5288c-110">Option d’URL simple 1</span><span class="sxs-lookup"><span data-stu-id="5288c-110">Simple URL Option 1</span></span>

<span data-ttu-id="5288c-111">Dans l’option 1, vous créez une nouvelle URL de base pour chaque URL simple.</span><span class="sxs-lookup"><span data-stu-id="5288c-111">In Option 1, you create a new base URL for each simple URL.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="5288c-112">Lorsqu’un utilisateur clique sur un lien de réunion d’URL simple, le serveur résolu par l’enregistrement DNS pour déterminer le logiciel client approprié à démarrer.</span><span class="sxs-lookup"><span data-stu-id="5288c-112">When a user clicks a simple URL meeting link, the server that the DNS A record resolves to determines the correct client software to start.</span></span> <span data-ttu-id="5288c-113">Lorsque le logiciel client est démarré, il communique automatiquement avec le pool sur lequel la Conférence est hébergée.</span><span class="sxs-lookup"><span data-stu-id="5288c-113">After the client software is started, it automatically communicates with the pool where the conference is hosted.</span></span> <span data-ttu-id="5288c-114">De cette façon, les utilisateurs sont dirigés vers le serveur approprié pour le contenu de la réunion, quel que soit le serveur ou le pool sur lequel les enregistrements sont résolus.</span><span class="sxs-lookup"><span data-stu-id="5288c-114">This way, users are directed to the appropriate server for meeting content no matter which server or pool the simple URL DNS A records resolve to.</span></span>



</div>

### <a name="simple-url-option-1"></a><span data-ttu-id="5288c-115">Option d’URL simple 1</span><span class="sxs-lookup"><span data-stu-id="5288c-115">Simple URL Option 1</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5288c-116"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-116"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="5288c-117"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-117"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-118">Correspondre</span><span class="sxs-lookup"><span data-stu-id="5288c-118">Meet</span></span></p></td>
<td><p><span data-ttu-id="5288c-119"> https://meet.contoso.com, https://meet.fabrikam.com et ainsi de suite (un pour chaque domaine SIP de votre organisation)</span><span class="sxs-lookup"><span data-stu-id="5288c-119">https://meet.contoso.com, https://meet.fabrikam.com, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5288c-120">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="5288c-120">Dial-in</span></span></p></td>
<td><p>https://dialin.contoso.com</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-121">Administrateur</span><span class="sxs-lookup"><span data-stu-id="5288c-121">Admin</span></span></p></td>
<td><p>https://admin.contoso.com</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5288c-122">Si vous utilisez l’option 1, vous devez définir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5288c-122">If you use Option 1, you must define the following:</span></span>

  - <span data-ttu-id="5288c-123">Pour chaque URL de la réunion, vous avez besoin d’un enregistrement DNS A qui résout l’URL en adresse IP du directeur, si vous en avez déployé une.</span><span class="sxs-lookup"><span data-stu-id="5288c-123">For each Meet simple URL, you need a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="5288c-124">Dans le cas contraire, elle doit résoudre vers l’adresse IP de l’équilibrage de charge d’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5288c-124">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="5288c-125">Si vous n’avez pas déployé de pool et que vous utilisez un déploiement Standard Edition Server, l’enregistrement DNS A doit résoudre vers l’adresse IP d’un serveur Standard Edition au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5288c-125">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>
    
    <span data-ttu-id="5288c-126">Si vous avez plusieurs domaines SIP au sein de votre organisation et que vous utilisez cette option, vous devez créer des URL d’URL simples pour chaque domaine SIP et vous avez besoin d’un enregistrement DNS A pour chaque URL de la réunion.</span><span class="sxs-lookup"><span data-stu-id="5288c-126">If you have more than one SIP domain in your organization and you use this option, you must create Meet simple URLs for each SIP domain and you need a DNS A record for each Meet simple URL.</span></span> <span data-ttu-id="5288c-127">Par exemple, si vous avez à la fois contoso.com et fabrikam.com, vous devez créer des enregistrements DNS A pour les deux https://meet.contoso.com et https://meet.fabrikam.com .</span><span class="sxs-lookup"><span data-stu-id="5288c-127">For example, if you have both contoso.com and fabrikam.com, you will create DNS A records for both https://meet.contoso.com and https://meet.fabrikam.com.</span></span>
    
    <span data-ttu-id="5288c-128">Par ailleurs, si vous avez plusieurs domaines SIP et que vous souhaitez réduire les exigences d’enregistrements DNS et de certificats pour ces URL simples, utilisez l’option 3 décrite plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5288c-128">Alternatively, if you have multiple SIP domains and you want to minimize the DNS record and certificate requirements for these simple URLs, use Option 3 as described later in this topic.</span></span>

  - <span data-ttu-id="5288c-129">Dans le cas de l’URL d’accès à la Conférence rendez-vous, vous avez besoin d’un enregistrement DNS A qui résout l’URL vers l’adresse IP du réalisateur, si vous en avez déployé une.</span><span class="sxs-lookup"><span data-stu-id="5288c-129">For the Dial-in simple URL, you need a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="5288c-130">Dans le cas contraire, elle doit résoudre vers l’adresse IP de l’équilibrage de charge d’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5288c-130">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="5288c-131">Si vous n’avez pas déployé de pool et que vous utilisez un déploiement Standard Edition Server, l’enregistrement DNS A doit résoudre vers l’adresse IP d’un serveur Standard Edition au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5288c-131">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

  - <span data-ttu-id="5288c-132">L’URL simple d’administration est réservée à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="5288c-132">The Admin simple URL is internal only.</span></span> <span data-ttu-id="5288c-133">Il nécessite un enregistrement DNS A qui résout l’URL vers l’adresse IP du directeur, si vous en avez déployé une.</span><span class="sxs-lookup"><span data-stu-id="5288c-133">It requires a DNS A record that resolves the URL to the IP address of the Director, if you have one deployed.</span></span> <span data-ttu-id="5288c-134">Dans le cas contraire, elle doit résoudre vers l’adresse IP de l’équilibrage de charge d’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5288c-134">Otherwise, it should resolve to the IP address of the load balancer of a Front End pool.</span></span> <span data-ttu-id="5288c-135">Si vous n’avez pas déployé de pool et que vous utilisez un déploiement Standard Edition Server, l’enregistrement DNS A doit résoudre vers l’adresse IP d’un serveur Standard Edition au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5288c-135">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

</div>

<div>

## <a name="simple-url-option-2"></a><span data-ttu-id="5288c-136">Option d’URL simple 2</span><span class="sxs-lookup"><span data-stu-id="5288c-136">Simple URL Option 2</span></span>

<span data-ttu-id="5288c-137">Avec l’option 2, les URL de base, de conférence rendez-vous et d’administration, telles que lync.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5288c-137">With Option 2, the Meet, Dial-in, and Admin simple URLs all have a common base URL, such as lync.contoso.com.</span></span> <span data-ttu-id="5288c-138">Par conséquent, vous n’avez besoin que d’un seul enregistrement DNS pour ces URL simples, ce qui a pour effet de répartir lync.contoso.com vers l’adresse IP d’un pool de réalisateurs ou d’un pool frontal.</span><span class="sxs-lookup"><span data-stu-id="5288c-138">Therefore, you need only one DNS A record for these simple URLs, which resolves lync.contoso.com to the IP address of a Director pool or Front End pool.</span></span> <span data-ttu-id="5288c-139">Si vous n’avez pas déployé de pool et que vous utilisez un déploiement Standard Edition Server, l’enregistrement DNS A doit résoudre vers l’adresse IP d’un serveur Standard Edition au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5288c-139">If you have not deployed a pool and are using a Standard Edition server deployment, the DNS A record must resolve to the IP address of one Standard Edition server in your organization.</span></span>

<span data-ttu-id="5288c-140">Notez que si vous avez plusieurs domaines SIP dans votre organisation, vous devez quand même créer des URL simples pour chaque domaine SIP et vous avez besoin d’un enregistrement DNS A pour chaque URL de la réunion.</span><span class="sxs-lookup"><span data-stu-id="5288c-140">Note that if you have more than one SIP domain in your organization, you must still create Meet simple URLs for each SIP domain and you need a DNS A record for each Meet simple URL.</span></span> <span data-ttu-id="5288c-141">Dans cet exemple, alors que trois URL simples sont basées sur lync.contoso.com, une URL simple de l’interface de fabrikam.com est configurée avec une autre URL de base.</span><span class="sxs-lookup"><span data-stu-id="5288c-141">In this example, while three simple URLs are all based on lync.contoso.com, an additional Meet simple URL for fabrikam.com is set up with a different base URL.</span></span> <span data-ttu-id="5288c-142">Dans cet exemple, vous devez créer des enregistrements DNS A pour les deux https://lync.contoso.com et https://lync.fabrikam.com .</span><span class="sxs-lookup"><span data-stu-id="5288c-142">In this example, you must create DNS A records for both https://lync.contoso.com and https://lync.fabrikam.com.</span></span> <span data-ttu-id="5288c-143">L’option simple d’URL 3 vous permet d’utiliser une autre méthode pour gérer l’attribution de noms et les enregistrements DNS A si vous avez plusieurs domaines SIP.</span><span class="sxs-lookup"><span data-stu-id="5288c-143">Simple URL Option 3 shows another way to handle naming and DNS A records if you have multiple SIP domains.</span></span>

### <a name="simple-url-option-2"></a><span data-ttu-id="5288c-144">Option d’URL simple 2</span><span class="sxs-lookup"><span data-stu-id="5288c-144">Simple URL Option 2</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5288c-145"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-145"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="5288c-146"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-146"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-147">Correspondre</span><span class="sxs-lookup"><span data-stu-id="5288c-147">Meet</span></span></p></td>
<td><p><span data-ttu-id="5288c-148"> https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet et ainsi de suite (un pour chaque domaine SIP de votre organisation)</span><span class="sxs-lookup"><span data-stu-id="5288c-148">https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5288c-149">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="5288c-149">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-150">Administrateur</span><span class="sxs-lookup"><span data-stu-id="5288c-150">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/Admin</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simple-url-option-3"></a><span data-ttu-id="5288c-151">Option d’URL simple 3</span><span class="sxs-lookup"><span data-stu-id="5288c-151">Simple URL Option 3</span></span>

<span data-ttu-id="5288c-152">L’option 3 est particulièrement utile si vous avez de nombreux domaines SIP et que vous souhaitez qu’ils disposent d’URL simples distinctes et qu’ils souhaitent limiter les exigences d’enregistrements DNS et de certificats pour ces URL simples.</span><span class="sxs-lookup"><span data-stu-id="5288c-152">Option 3 is most useful if you have many SIP domains, and you want them to have separate simple URLs but want to minimize the DNS record and certificate requirements for these simple URLs.</span></span> <span data-ttu-id="5288c-153">Dans cet exemple, vous avez besoin d’un enregistrement DNS A unique, qui résout lync.contoso.com sur l’adresse IP d’un pool de réalisateurs ou d’une liste frontale.</span><span class="sxs-lookup"><span data-stu-id="5288c-153">In this example, you need only one DNS A record, which resolves lync.contoso.com to the IP address of a Director pool or Front End pool.</span></span>

### <a name="simple-url-option-3"></a><span data-ttu-id="5288c-154">Option d’URL simple 3</span><span class="sxs-lookup"><span data-stu-id="5288c-154">Simple URL Option 3</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5288c-155"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-155"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="5288c-156"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="5288c-156"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-157">Correspondre</span><span class="sxs-lookup"><span data-stu-id="5288c-157">Meet</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Meet</p>
<p>https://lync.contoso.com/fabrikamSIPdomain/Meet</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5288c-158">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="5288c-158">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5288c-159">Administrateur</span><span class="sxs-lookup"><span data-stu-id="5288c-159">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Admin</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="disaster-recovery-option-for-simple-urls"></a><span data-ttu-id="5288c-160">Option de reprise après sinistre pour les URL simples</span><span class="sxs-lookup"><span data-stu-id="5288c-160">Disaster Recovery Option for Simple URLs</span></span>

<span data-ttu-id="5288c-161">Si vous disposez de plusieurs sites et que votre fournisseur DNS prend en charge GeoDNS, vous pouvez configurer vos enregistrements DNS pour des URL simples afin de prendre en charge la reprise après sinistre, afin que la fonctionnalité d’URL n’intervient qu’à la fin de l’exécution d’un pool frontal complet.</span><span class="sxs-lookup"><span data-stu-id="5288c-161">If you have multiple sites that contain Front End pools and your DNS provider supports GeoDNS, you can set up your DNS records for Simple URLs to support disaster recovery, so that Simple URL functionality continues even if one entire Front End pool goes down.</span></span> <span data-ttu-id="5288c-162">Cette fonctionnalité de reprise après sinistre prend en charge les URL de la réunion et du rendez-vous simples.</span><span class="sxs-lookup"><span data-stu-id="5288c-162">This disaster recovery feature supports the Meet and Dial-In simple URLs.</span></span>

<span data-ttu-id="5288c-163">Pour le configurer, créez deux adresses GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="5288c-163">To configure this, create two GeoDNS addresses.</span></span> <span data-ttu-id="5288c-164">Chaque adresse possède deux enregistrements DNS A ou CNAMe qui sont résolus en deux regroupements qui sont associés à des fins de récupération par sinistre.</span><span class="sxs-lookup"><span data-stu-id="5288c-164">Each address has two DNS A or CNAME records that resolve to two pools which are paired together for disaster recovery purposes.</span></span> <span data-ttu-id="5288c-165">Une adresse GeoDNS est utilisée pour l’accès interne et est résolue vers l’adresse IP du nom de domaine complet ou du nom de domaine complet (FQDN) du site Web interne.</span><span class="sxs-lookup"><span data-stu-id="5288c-165">One GeoDNS address is used for internal access, and resolves to the internal web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="5288c-166">L’autre adresse GeoDNS est utilisée pour l’accès externe et est résolue sur l’adresse IP de nom de domaine complet ou du nom de domaine complet des deux pools.</span><span class="sxs-lookup"><span data-stu-id="5288c-166">The other GeoDNS address is used for external access and resolves to the external web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="5288c-167">Voici un exemple de l’URL de la réunion, en utilisant les noms de domaine complets (FQDN) pour les pools.</span><span class="sxs-lookup"><span data-stu-id="5288c-167">The following is an example for the Meet simple URL, using the FQDNs for the pools.</span></span>

   ```console
    Meet-int.geolb.contoso.com
         Pool1InternalWebFQDN.contoso.com
         Pool2InternalWebFQDN.contoso.com
   ```

   ```console
   Meet-ext.geolb.contoso.com
         Pool1ExternalWebFQDN.contoso.com
         Pool2ExternalWebFQDN.contoso.com
   ``` 

<span data-ttu-id="5288c-168">Ensuite, créez des enregistrements CNAMe qui résolvent votre URL de réunion simple (par exemple, meet.contoso.com) sur les deux adresses GeoDNS.</span><span class="sxs-lookup"><span data-stu-id="5288c-168">Then create CNAME records that resolve your Meet simple URL (such as meet.contoso.com) to the two GeoDNS addresses.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="5288c-169">Si votre réseau utilise <EM>Hairpinning</EM> (le routage de tout le trafic d’URL par le biais du lien externe, y compris le trafic qui provient de votre organisation), vous pouvez simplement configurer l’adresse GeoDNS externe et résoudre votre URL de la réunion pour qu’elle utilise uniquement cette adresse externe.</span><span class="sxs-lookup"><span data-stu-id="5288c-169">If your network uses <EM>hairpinning</EM> (routing all your Simple URL traffic through the external link, including traffic that comes from within your organization), then you can just configure the external GeoDNS address and resolve your Meet simple URL to only that external address.</span></span>



</div>

<span data-ttu-id="5288c-170">Lorsque vous utilisez cette méthode, vous pouvez configurer chaque adresse GeoDNS pour utiliser une méthode de tourniquet circulaire pour distribuer les demandes aux deux pools, ou pour vous connecter principalement à un pool (par exemple, le pool localisé plus près) et utiliser l’autre pool uniquement en cas d’échec de connectivité.</span><span class="sxs-lookup"><span data-stu-id="5288c-170">When you use this method, you can configure each GeoDNS address to use either a round robin method to distribute requests to the two pools, or to connect primarily to one pool (such as the pool located geographically closer) and use the other pool only in case of connectivity failure.</span></span>

<span data-ttu-id="5288c-171">Vous pouvez configurer la même configuration pour l’URL d’accès à la Conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="5288c-171">You can set up the same configuration for the Dial-In simple URL.</span></span> <span data-ttu-id="5288c-172">Pour ce faire, créez des enregistrements supplémentaires comme ceux de l’exemple précédent, `dialin` en remplaçant `meet` les enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="5288c-172">To do so, create additional records like those in the previous example, substituting `dialin` for `meet` in the DNS records.</span></span> <span data-ttu-id="5288c-173">Pour l’URL simple d’administration, utilisez l’une des trois options indiquées plus haut dans cette section.</span><span class="sxs-lookup"><span data-stu-id="5288c-173">For the Admin simple URL, use one of the three options listed earlier in this section.</span></span>

<span data-ttu-id="5288c-174">Une fois cette configuration configurée, vous devez utiliser une application de surveillance pour configurer la surveillance HTTP et surveiller les échecs.</span><span class="sxs-lookup"><span data-stu-id="5288c-174">Once this configuration is set up, you must use a monitoring application to set up HTTP monitoring to watch for failures.</span></span> <span data-ttu-id="5288c-175">Pour un accès externe, assurez-vous que les demandes de découverte automatique associées à l’adresse IP du nom de domaine complet ou du nom de domaine complet des deux pools sont correctes.</span><span class="sxs-lookup"><span data-stu-id="5288c-175">For external access, monitor to make sure that HTTPS GET autodiscovery requests to the external web FQDN or load balancer IP address for the two pools are successful.</span></span> <span data-ttu-id="5288c-176">Par exemple, les requêtes suivantes ne doivent pas contenir d’en-tête **Accept** et doivent retourner **200 OK**.</span><span class="sxs-lookup"><span data-stu-id="5288c-176">For example, the following requests must not contain any **ACCEPT** header and must return **200 OK**.</span></span>

```console
    HTTPS GET Pool1ExternalWebFQDN.contoso.com/autodiscover/autodiscoverservice.svc/root
    HTTPS GET Pool2ExternalWebFQDN.contoso.com/autodiscover/autodiscoverservice.svc/root
```

<span data-ttu-id="5288c-177">Pour un accès interne, vous devez surveiller le port 5061 sur l’adresse IP du nom de domaine complet (FQDN) du site Web interne ou du solde de charge des deux pools.</span><span class="sxs-lookup"><span data-stu-id="5288c-177">For internal access, you must monitor port 5061 on the internal web FQDN or load balancer IP address for the two pools.</span></span> <span data-ttu-id="5288c-178">Si des échecs de connectivité sont détectés, l’adresse VIP de ces groupes doit fermer les ports 80, 443 et 444.</span><span class="sxs-lookup"><span data-stu-id="5288c-178">If any connectivity failures are detected, the VIP for these pools must close ports 80, 443 and 444.</span></span>

<span data-ttu-id="5288c-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5288c-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

