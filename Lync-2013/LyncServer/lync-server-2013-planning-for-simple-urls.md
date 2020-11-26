---
title: 'Lync Server 2013 : Planification des URL simples'
description: 'Lync Server 2013 : planification d’URL simples.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for simple URLs
ms:assetid: 20e4f4b6-b7ff-4297-b00d-d1211ee800ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398287(v=OCS.15)
ms:contentKeyID: 48183610
ms.date: 12/12/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10a7f2aaf85dafe5facba7cfd2509cfcc8812d67
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442879"
---
# <a name="planning-for-simple-urls-in-lync-server-2013"></a><span data-ttu-id="f74b3-103">Planification des URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f74b3-103">Planning for simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f74b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f74b3-104">

<span> </span></span></span>

<span data-ttu-id="f74b3-105">_**Dernière modification de la rubrique :** 2015-12-11_</span><span class="sxs-lookup"><span data-stu-id="f74b3-105">_**Topic Last Modified:** 2015-12-11_</span></span>

<span data-ttu-id="f74b3-106">Les URL simples permettent de participer plus facilement à des réunions pour vos utilisateurs et permettent d’accéder plus facilement aux outils d’administration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f74b3-106">Simple URLs make joining meetings easier for your users, and make getting to Lync Server administrative tools easier for your administrators.</span></span>

<span data-ttu-id="f74b3-107">Lync Server prend en charge trois URL simples :</span><span class="sxs-lookup"><span data-stu-id="f74b3-107">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="f74b3-108">La **fonction réunion** est utilisée comme URL de base pour toutes les conférences du site ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-108">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="f74b3-109">Par exemple, une URL de réunion simple est https://meet.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="f74b3-109">An example of a Meet simple URL is https://meet.contoso.com.</span></span> <span data-ttu-id="f74b3-110">Une URL pour une réunion particulière peut être https://meet.contoso.com/ *nom d’utilisateur*/7322994.</span><span class="sxs-lookup"><span data-stu-id="f74b3-110">A URL for a particular meeting might be https://meet.contoso.com/*username*/7322994.</span></span>
    
    <span data-ttu-id="f74b3-111">Avec l’URL de la réunion, vous pouvez facilement comprendre les liens permettant de participer à des réunions, et facilement communiquer et diffuser.</span><span class="sxs-lookup"><span data-stu-id="f74b3-111">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="f74b3-112">Le rendez **-** vous permet d’accéder à la page Web des paramètres de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="f74b3-112">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="f74b3-113">Cette page présente les numéros de conférence rendez-vous en fonction de la langue disponible, des informations de conférence affectées (c’est-à-dire pour les réunions qui n’ont pas besoin d’être planifiées) et de contrôles DTMF en conférence, et prend en charge la gestion de votre code confidentiel (PIN) et des informations de conférence affectées.</span><span class="sxs-lookup"><span data-stu-id="f74b3-113">This page displays conference dial-in numbers with their available languages, assigned conference information (that is, for meetings that do not need to be scheduled), and in-conference DTMF controls, and supports management of personal identification number (PIN) and assigned conferencing information.</span></span> <span data-ttu-id="f74b3-114">L’URL d’accès à un rendez-vous est incluse dans toutes les invitations à une réunion de sorte que les utilisateurs qui souhaitent se connecter à la réunion puissent accéder au numéro de téléphone et aux informations de code confidentiel nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f74b3-114">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span> <span data-ttu-id="f74b3-115">Par exemple, l’URL de connexion simple est https://dialin.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="f74b3-115">An example of the Dial-in simple URL is https://dialin.contoso.com.</span></span>

  - <span data-ttu-id="f74b3-116">L' **administrateur** vous permet d’accéder rapidement au panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f74b3-116">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="f74b3-117">À partir de n’importe quel ordinateur au sein des pare-feu de votre organisation, un administrateur peut ouvrir le panneau de configuration de Lync Server en entrant l’URL simple d’administration dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="f74b3-117">From any computer within your organization’s firewalls, an admin can open the Lync Server Control Panel by typing the Admin simple URL into a browser.</span></span> <span data-ttu-id="f74b3-118">L’URL simple Admin est interne à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-118">The Admin simple URL is internal to your organization.</span></span> <span data-ttu-id="f74b3-119">Par exemple, l’URL d’administration simple est https://admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f74b3-119">An example of the Admin simple URL is https://admin.contoso.com</span></span>

<div>

## <a name="simple-url-scope"></a><span data-ttu-id="f74b3-120">Étendue d’URL simple</span><span class="sxs-lookup"><span data-stu-id="f74b3-120">Simple URL Scope</span></span>

<span data-ttu-id="f74b3-121">Vous pouvez configurer vos URL simples pour qu’elles aient une étendue globale ou spécifier différentes URL simples pour chaque site central de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-121">You can configure your simple URLs to have global scope, or you can specify different simple URLs for each central site in your organization.</span></span> <span data-ttu-id="f74b3-122">S’il s’agit d’une URL simple d’étendue globale et d’une URL simple d’étendue de site, l’URL d’étendue du site est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="f74b3-122">If both a global scope simple URL and a site scope simple URL are specified, the site scope simple URL has precedence.</span></span>

<span data-ttu-id="f74b3-123">Dans la plupart des cas, nous vous conseillons de définir des URL simples uniquement au niveau global, de telle sorte que l’URL de la réunion n’est pas la même que celle d’un site à l’autre.</span><span class="sxs-lookup"><span data-stu-id="f74b3-123">In most cases, we recommend that you set simple URLs only at the global level, so that a user’s Meet simple URL does not change if they move from one site to another.</span></span> <span data-ttu-id="f74b3-124">Il peut s’agir d’organisations qui ont besoin d’utiliser différents numéros de téléphone pour les utilisateurs rendez-vous sur différents sites.</span><span class="sxs-lookup"><span data-stu-id="f74b3-124">The exception would be organizations that need to use different telephone numbers for dial-in users at different sites.</span></span> <span data-ttu-id="f74b3-125">Notez que si vous définissez une URL simple (par exemple, l’URL d’accès à la Conférence rendez-vous) sur un site, vous devez également définir d’autres URL simples sur ce site comme niveau de site.</span><span class="sxs-lookup"><span data-stu-id="f74b3-125">Note that if you set one simple URL (such as the Dial-in simple URL) at a site to be a site-level simple URL, you must also set the other simple URLs at that site to be site-level as well.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f74b3-126">Si vous choisissez d’utiliser des URL simples à portée de site, vos utilisateurs ne seront pas en mesure de basculer entre les pools de Front-End dans les différents sites sans que les utilisateurs replanifient toutes leurs réunions planifiées, car les URL simples de la réunion sont différentes entre les sites.</span><span class="sxs-lookup"><span data-stu-id="f74b3-126">If you choose to use site scoped simple URLs, your users won't be able to move between Front-End pools in different sites without those users rescheduling all of their scheduled meetings as the meeting simple URLs are different between sites.</span></span> <span data-ttu-id="f74b3-127">Cela inclut les scénarios de basculement dans lesquels les relations de sauvegarde se trouvent dans des sites distincts.</span><span class="sxs-lookup"><span data-stu-id="f74b3-127">This includes fail-over scenarios where pools in backup relationships are in separate sites.</span></span> <span data-ttu-id="f74b3-128">Lorsque vous avez besoin de basculer entre les sites dans lesquels les URL simples de votre site sont déployées, les utilisateurs ne seront pas en mesure de rejoindre leurs réunions en raison de l’étendue de l’URL.</span><span class="sxs-lookup"><span data-stu-id="f74b3-128">When you need to fail-over between sites where site scoped simple URLs are deployed, users won't be able to join their meetings because of the scope for URL.</span></span> <span data-ttu-id="f74b3-129">Pour plus d’informations, consultez <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsSimpleUrlConfiguration">Get-CsSimpleUrlConfiguration</A>.</span><span class="sxs-lookup"><span data-stu-id="f74b3-129">For further information, check <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsSimpleUrlConfiguration">Get-CsSimpleUrlConfiguration</A>.</span></span>



</div>

<span data-ttu-id="f74b3-130">Vous pouvez définir des URL simples globales dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="f74b3-130">You can set global simple URLs in Topology Builder.</span></span> <span data-ttu-id="f74b3-131">Pour définir une URL simple au niveau du site, vous devez utiliser l’applet de Set-CsSimpleURLConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f74b3-131">To set a simple URL at the site level, you must use the Set-CsSimpleURLConfiguration cmdlet.</span></span>

</div>

<div>

## <a name="naming-your-simple-urls"></a><span data-ttu-id="f74b3-132">Attribution d’un nom à vos URL simples</span><span class="sxs-lookup"><span data-stu-id="f74b3-132">Naming Your Simple URLs</span></span>

<span data-ttu-id="f74b3-133">Il existe trois options recommandées pour nommer vos URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-133">There are three recommended options for naming your simple URLs.</span></span> <span data-ttu-id="f74b3-134">L’option que vous choisissez a des implications sur la configuration de vos enregistrements DNS A et des certificats qui prennent en charge des URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-134">Which option you choose has implications for how you set up your DNS A records and certificates which support simple URLs.</span></span> <span data-ttu-id="f74b3-135">Dans chaque option, vous devez configurer une seule URL de la réunion pour chaque domaine SIP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-135">In each option, you must configure one Meet simple URL for each SIP domain in your organization.</span></span>

<span data-ttu-id="f74b3-136">Vous avez toujours besoin d’une seule URL dans l’ensemble de votre organisation pour le rendez-vous, et l’autre pour l’administrateur, quel que soit le nombre de domaines SIP.</span><span class="sxs-lookup"><span data-stu-id="f74b3-136">You always need just one simple URL in your whole organization for Dial-in, and one for Admin, no matter how many SIP domains you have.</span></span>

<span data-ttu-id="f74b3-137">Pour plus d’informations sur les enregistrements et les certificats DNS requis, voir [exigences DNS pour les URL simples dans Lync server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) et les [certificats requis pour les serveurs internes dans Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="f74b3-137">For details about the necessary DNS A records and certificates, see [DNS requirements for simple URLs in Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) and [Certificate requirements for internal servers in Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in the Planning documentation.</span></span>

<span data-ttu-id="f74b3-138">Dans l’option 1, vous créez un nouveau nom de domaine SIP pour chaque URL simple.</span><span class="sxs-lookup"><span data-stu-id="f74b3-138">In Option 1, you create a new SIP domain name for each simple URL.</span></span>

<span data-ttu-id="f74b3-139">Si vous utilisez cette option, vous avez besoin d’un enregistrement DNS A distinct pour chaque URL simple et chaque URL de la réunion doit être nommée dans vos certificats.</span><span class="sxs-lookup"><span data-stu-id="f74b3-139">If you use this option, you need a separate DNS A record for each simple URL, and each Meet simple URL must be named in your certificates.</span></span>

### <a name="simple-url-naming-option-1"></a><span data-ttu-id="f74b3-140">Option de nom d’URL simple 1</span><span class="sxs-lookup"><span data-stu-id="f74b3-140">Simple URL Naming Option 1</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-141"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-141"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="f74b3-142"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-142"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-143">Correspondre</span><span class="sxs-lookup"><span data-stu-id="f74b3-143">Meet</span></span></p></td>
<td><p><span data-ttu-id="f74b3-144"> https://meet.contoso.com, https://meet.fabrikam.com et ainsi de suite (un pour chaque domaine SIP de votre organisation)</span><span class="sxs-lookup"><span data-stu-id="f74b3-144">https://meet.contoso.com, https://meet.fabrikam.com, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-145">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f74b3-145">Dial-in</span></span></p></td>
<td><p>https://dialin.contoso.com</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-146">Administrateur</span><span class="sxs-lookup"><span data-stu-id="f74b3-146">Admin</span></span></p></td>
<td><p>https://admin.contoso.com</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f74b3-147">Avec l’option 2, les URL simples sont basées sur le nom de domaine lync.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="f74b3-147">With Option 2, simple URLs are based on the domain name lync.contoso.com.</span></span> <span data-ttu-id="f74b3-148">Par conséquent, vous avez besoin d’un enregistrement DNS A qui active les trois types d’URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-148">Therefore, you need only one DNS A record which enables all three types of simple URLs.</span></span> <span data-ttu-id="f74b3-149">Cet enregistrement DNS A fait référence à lync.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="f74b3-149">This DNS A record references lync.contoso.com.</span></span> <span data-ttu-id="f74b3-150">Par ailleurs, vous avez encore besoin d’enregistrements DNS A séparés pour d’autres domaines SIP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-150">Additionally, you still need separate DNS A records for other SIP domains in your organization.</span></span>

### <a name="simple-url-naming-option-2"></a><span data-ttu-id="f74b3-151">Option de nom d’URL simple 2</span><span class="sxs-lookup"><span data-stu-id="f74b3-151">Simple URL Naming Option 2</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-152"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-152"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="f74b3-153"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-153"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-154">Correspondre</span><span class="sxs-lookup"><span data-stu-id="f74b3-154">Meet</span></span></p></td>
<td><p><span data-ttu-id="f74b3-155"> https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet et ainsi de suite (un pour chaque domaine SIP de votre organisation)</span><span class="sxs-lookup"><span data-stu-id="f74b3-155">https://lync.contoso.com/Meet, https://lync.fabrikam.com/Meet, and so on (one for each SIP domain in your organization)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-156">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f74b3-156">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-157">Administrateur</span><span class="sxs-lookup"><span data-stu-id="f74b3-157">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/Admin</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f74b3-158">L’option 3 est particulièrement utile si vous avez de nombreux domaines SIP et que vous souhaitez qu’ils soient séparés par des URL simples et qu’ils souhaitent limiter les exigences d’enregistrements DNS et de certificats pour ces URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-158">Option 3 is most useful if you have many SIP domains, and you want them to have separate Meet simple URLs but want to minimize the DNS record and certificate requirements for these simple URLs.</span></span>

### <a name="simple-url-naming-option-3"></a><span data-ttu-id="f74b3-159">Option de nom d’URL simple 3</span><span class="sxs-lookup"><span data-stu-id="f74b3-159">Simple URL Naming Option 3</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-160"><strong>URL simple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-160"><strong>Simple URL</strong></span></span></p></td>
<td><p><span data-ttu-id="f74b3-161"><strong>Exemple</strong></span><span class="sxs-lookup"><span data-stu-id="f74b3-161"><strong>Example</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-162">Correspondre</span><span class="sxs-lookup"><span data-stu-id="f74b3-162">Meet</span></span></p></td>
<td><p>https://lync.contoso.com/contosoSIPdomain/Meet</p>
<p>https://lync.contoso.com/fabrikamSIPdomain/Meet</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f74b3-163">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="f74b3-163">Dial-in</span></span></p></td>
<td><p>https://lync.contoso.com/Dialin</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f74b3-164">Administrateur</span><span class="sxs-lookup"><span data-stu-id="f74b3-164">Admin</span></span></p></td>
<td><p>https://lync.contoso.com/Admin</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="simple-url-naming-and-validation-rules"></a><span data-ttu-id="f74b3-165">Règles de validation et d’attribution d’URL simples</span><span class="sxs-lookup"><span data-stu-id="f74b3-165">Simple URL Naming and Validation Rules</span></span>

<span data-ttu-id="f74b3-166">Le générateur de topologie et les applets de contrôle Lync Server Management Shell appliquent plusieurs règles de validation pour vos URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-166">Topology Builder and the Lync Server Management Shell cmdlets enforce several validation rules for your simple URLs.</span></span> <span data-ttu-id="f74b3-167">Vous devez définir des URL simples pour la réunion et le numéro de téléphone, mais la définition d’une pour l’administrateur est facultative.</span><span class="sxs-lookup"><span data-stu-id="f74b3-167">You are required to set simple URLs for Meet and Dialin, but setting one for Admin is optional.</span></span> <span data-ttu-id="f74b3-168">Chaque domaine SIP doit être doté d’une URL simple de connexion, mais vous n’avez besoin que d’une seule URL de composition unique et d’une URL simple d’administration pour l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f74b3-168">Each SIP domain must have a separate Meet simple URL, but you need only one Dialin simple URL and one Admin simple URL for your whole organization.</span></span>

<span data-ttu-id="f74b3-169">Chaque URL simple de votre organisation doit avoir un nom unique et ne peut pas être un préfixe d’une autre URL simple (par exemple, vous n’avez pas pu définir lync.contoso.com/Meet comme URL simple de la Conférence).</span><span class="sxs-lookup"><span data-stu-id="f74b3-169">Each simple URL in your organization must have a unique name, and cannot be a prefix of another simple URL (for example, you could not set lync.contoso.com/Meet as your Meet simple URL and lync.contoso.com/Meet/Dialin as your Dialin simple URL).</span></span> <span data-ttu-id="f74b3-170">Les noms d’URL simples ne peuvent pas contenir le nom de domaine complet de l’un de vos groupes, ni aucune information de port (par exemple, https://FQDN:88/meet n’est pas autorisée).</span><span class="sxs-lookup"><span data-stu-id="f74b3-170">Simple URL names cannot contain the FQDN of any of your pools, or any port information (for example, https://FQDN:88/meet is not allowed).</span></span> <span data-ttu-id="f74b3-171">Toutes les URL simples doivent commencer par le préfixe https://.</span><span class="sxs-lookup"><span data-stu-id="f74b3-171">All simple URLs must start with the https:// prefix.</span></span>

<span data-ttu-id="f74b3-172">Les URL simples peuvent contenir des caractères alphanumériques (c’est-à-dire, a-z, A-Z, 0-9 et le point (.).</span><span class="sxs-lookup"><span data-stu-id="f74b3-172">Simple URLs can contain only alphanumeric characters (that is, a-z, A-Z, 0-9, and the period (.).</span></span> <span data-ttu-id="f74b3-173">Si vous utilisez d’autres caractères, les URL simples risquent de ne pas fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="f74b3-173">If you use other characters, the simple URLs might not work as expected.</span></span>

</div>

<div>

## <a name="changing-simple-urls-after-deployment"></a><span data-ttu-id="f74b3-174">Modification d’URL simples après le déploiement</span><span class="sxs-lookup"><span data-stu-id="f74b3-174">Changing Simple URLs after Deployment</span></span>

<span data-ttu-id="f74b3-175">Si vous modifiez une URL simple après le déploiement initial, vous devez tenir compte de la façon dont le changement a un impact sur vos enregistrements DNS et les certificats pour les URL simples.</span><span class="sxs-lookup"><span data-stu-id="f74b3-175">If you change a simple URL after initial deployment, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="f74b3-176">Si la base d’une URL simple change, vous devez également modifier les enregistrements DNS et les certificats.</span><span class="sxs-lookup"><span data-stu-id="f74b3-176">If the base of a simple URL changes, then you must change the DNS records and certificates as well.</span></span> <span data-ttu-id="f74b3-177">Par exemple, https://lync.contoso.com/Meet https://meet.contoso.com si vous modifiez l’URL de base de lync.contoso.com à Meet.contoso.com, vous devez modifier les enregistrements DNS et les certificats pour faire référence à Meet.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="f74b3-177">For example, changing from https://lync.contoso.com/Meet to https://meet.contoso.com changes the base URL from lync.contoso.com to meet.contoso.com, so you would need to change the DNS records and certificates to refer to meet.contoso.com.</span></span> <span data-ttu-id="f74b3-178">Si vous avez changé l’URL simple de https://lync.contoso.com/Meet à https://lync.contoso.com/Meetings , l’URL de base de Lync.contoso.com reste inchangée et aucune modification du DNS ou du certificat n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f74b3-178">If you changed the simple URL from https://lync.contoso.com/Meet to https://lync.contoso.com/Meetings, the base URL of lync.contoso.com stays the same, so no DNS or certificate changes are needed.</span></span>

<span data-ttu-id="f74b3-179">Néanmoins, chaque fois que vous modifiez un nom d’URL simple, vous devez exécuter **Enable-CsComputer** sur chaque réalisateur et serveur frontal pour enregistrer la modification.</span><span class="sxs-lookup"><span data-stu-id="f74b3-179">Whenever you change a simple URL name, however, you must run **Enable-CsComputer** on each Director and Front End Server to register the change.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f74b3-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f74b3-180">See Also</span></span>


[<span data-ttu-id="f74b3-181">Enregistrements DNS requis pour les URL simples dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f74b3-181">DNS requirements for simple URLs in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-simple-urls.md)  
  

<span data-ttu-id="f74b3-182"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f74b3-182"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

