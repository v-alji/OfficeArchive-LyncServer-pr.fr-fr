---
title: 'Lync Server 2013 : Création d’enregistrements DNS pour le service de découverte automatique'
description: 'Lync Server 2013 : création d’enregistrements DNS pour le service de découverte automatique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating DNS records for the Autodiscover Service
ms:assetid: 3756ffe4-c6b1-492d-850e-42a832e06567
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690010(v=OCS.15)
ms:contentKeyID: 48183823
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6903e6b07001289db8b65e8cc962e8d8db4b248b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431511"
---
# <a name="creating-dns-records-for-the-autodiscover-service-in-lync-server-2013"></a><span data-ttu-id="93b23-103">Création d’enregistrements DNS pour le service de découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93b23-103">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93b23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93b23-104">

<span> </span></span></span>

<span data-ttu-id="93b23-105">_**Dernière modification de la rubrique :** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="93b23-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="93b23-106">Vos utilisateurs mobiles Lync vous auront besoin d’activer la découverte automatique, et d’une partie de la création d’enregistrements DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="93b23-106">Your Lync Mobile users will need you to enable autodiscovery, and a part of that involves creating some Domain Name System (DNS) records.</span></span> <span data-ttu-id="93b23-107">En fonction de vos besoins, vous devez disposer des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="93b23-107">Depending on your needs, you need the following:</span></span>

  - <span data-ttu-id="93b23-108">Un enregistrement DNS interne pour prendre en charge les utilisateurs mobiles qui se connectent au sein du réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="93b23-108">An internal DNS record to support mobile users who’re connecting from within your organization's network.</span></span>

  - <span data-ttu-id="93b23-109">Enregistrement DNS externe ou public permettant de prendre en charge les utilisateurs mobiles qui se connectent à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="93b23-109">An external, or public, DNS record to support mobile users who’re connecting from the Internet</span></span>

<span data-ttu-id="93b23-110">Pourquoi ?</span><span class="sxs-lookup"><span data-stu-id="93b23-110">Why both?</span></span> <span data-ttu-id="93b23-111">Vous devez créer un enregistrement DNS interne et un enregistrement DNS externe pour chaque domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="93b23-111">You need to create both an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="93b23-112">Les enregistrements DNS que vous créez peuvent être des enregistrements de type (hôte) ou CNAMe.</span><span class="sxs-lookup"><span data-stu-id="93b23-112">The DNS records you create can be either A (host) records or CNAME records.</span></span> <span data-ttu-id="93b23-113">Pour vous aider, nous allons découvrir comment créer ces enregistrements DNS internes et externes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="93b23-113">To help you out, we’ll walk through how to create these internal and external DNS records below.</span></span> <span data-ttu-id="93b23-114">Pour plus d’informations sur la configuration requise pour les utilisateurs mobiles, vous pouvez consulter les [exigences techniques en matière de mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="93b23-114">If you need to do some further reading about the DNS requirements for mobile users, you can check out [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

<div>

## <a name="creating-an-internal-dns-cname-record"></a><span data-ttu-id="93b23-115">Création d’un enregistrement CNAMe DNS interne</span><span class="sxs-lookup"><span data-stu-id="93b23-115">Creating an internal DNS CNAME record</span></span>

1.  <span data-ttu-id="93b23-116">Pour créer un enregistrement DNS interne, vous devez vous connecter à un serveur DNS dans votre réseau à l’aide d’un compte de domaine membre du groupe administrateurs de domaine ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="93b23-116">To make an internal DNS record, you’ll need to log on to a DNS server in your network with a domain account that’s either a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="93b23-117">Ouvrez le composant logiciel enfichable d’administration DNS : cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="93b23-117">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="93b23-118">Dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour le domaine Active Directory sur lequel se trouve votre pool de directeurs et votre pool de serveurs Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-118">In the console tree of the DNS server, expand **Forward Lookup Zones** for the Active Directory domain where your Lync Server 2013 Director pool and Front End pool are installed.</span></span> <span data-ttu-id="93b23-119">(par exemple, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93b23-119">(for example, contoso.local).</span></span>

4.  <span data-ttu-id="93b23-120">Pour savoir si un enregistrement hôte A (AAAA pour IPv6) existe pour votre pool de Directors pour un enregistrement DNS interne, un enregistrement A doit exister pour le nom de domaine complet (FQDN) des services Web internes pour votre pool de répertoires (par exemple, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93b23-120">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="93b23-121">Si ce n’est pas le cas, il est possible que vous n’utilisiez pas un pool de directeurs et que vous deviez utiliser le nom de domaine complet (FQDN) du pool frontal ou même du nom de domaine complet (FQDN) du serveur pour votre installation.</span><span class="sxs-lookup"><span data-stu-id="93b23-121">If it’s not here, you may not be using a Director pool, and you’ll need to use the FQDN for your Front End pool or even a single server FQDN, if that’s your setup.</span></span>

5.  <span data-ttu-id="93b23-122">Tout en gardant à l’esprit que vous devez vérifier qu’il existe un enregistrement A (AAAA pour IPv6) pour votre pool frontal pour un enregistrement DNS interne, un enregistrement hôte A (ou AAAA) devrait exister pour le nom de domaine complet (FQDN) des services Web internes de votre liste frontale (par exemple, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93b23-122">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="93b23-123">Si ce n’est pas le cas, vous devez noter le nom de domaine complet (FQDN) du serveur frontal ou du serveur Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="93b23-123">If it doesn’t, you’ll need to make note of the FQDN for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="93b23-124">Lorsque vous savez quels sont les enregistrements d’hôte A (ou AAAA), dans l’arborescence de la console de votre serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="93b23-124">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="93b23-125">Cliquez avec le bouton droit sur le nom de domaine SIP, puis cliquez sur **Nouvel alias (CNAME)**.</span><span class="sxs-lookup"><span data-stu-id="93b23-125">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="93b23-126">Dans **nom** de l’alias, tapez lyncdiscoverinternal comme nom d’hôte de l’URL du service de découverte automatique interne.</span><span class="sxs-lookup"><span data-stu-id="93b23-126">In **Alias name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="93b23-127">Dans **nom de domaine complet (FQDN) de l’hôte cible**, tapez ou accédez au nom de domaine complet des services Web internes de votre pool de répertoires (par exemple, lyncwebdir01. contoso. local), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="93b23-127">In **Fully qualified domain name (FQDN) for target host**, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local) and then click **OK**.</span></span>

10. <span data-ttu-id="93b23-128">Vous devez créer un enregistrement CNAMe de découverte automatique dans la zone de recherche directe de chaque domaine SIP que vous prenez en charge dans votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-128">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-cname-record"></a><span data-ttu-id="93b23-129">Création d’un enregistrement CNAMe DNS externe</span><span class="sxs-lookup"><span data-stu-id="93b23-129">Creating an external DNS CNAME record</span></span>

1.  <span data-ttu-id="93b23-130">Pour créer un enregistrement CNAMe DNS externe, vous devez vous connecter à votre fournisseur DNS public, puis suivre les étapes décrites dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="93b23-130">To create an external DNS CNAME record, you’re going to need to connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="93b23-131">Nous ne sommes pas en mesure de décrire exactement l’endroit où se trouvent les éléments de l’environnement de votre fournisseur DNS, car il existe peut-être différentes manières de gérer votre DNS externe, mais nous espérons pouvoir suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="93b23-131">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="93b23-132">Connectez-vous à votre fournisseur DNS externe à l’aide d’un compte qui peut créer des enregistrements DNS dans cet environnement.</span><span class="sxs-lookup"><span data-stu-id="93b23-132">Log into your external DNS provider with an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="93b23-133">Un domaine SIP doit déjà être créé pour cet environnement.</span><span class="sxs-lookup"><span data-stu-id="93b23-133">You should have a SIP domain created for this environment already.</span></span> <span data-ttu-id="93b23-134">Développez la **zone de recherche directe** pour ce domaine SIP ou sélectionnez-la en fonction de l’interface DNS externe utilisée.</span><span class="sxs-lookup"><span data-stu-id="93b23-134">Expand the **Forward Lookup Zone** for this SIP domain, or otherwise select it depending on the external DNS interface being used.</span></span>

4.  <span data-ttu-id="93b23-135">Vous devez déjà voir l’enregistrement d’un hôte A (AAAA pour IPv6) pour votre pool de réalisateurs (par exemple, lyncwebexdir01.contoso.com), alors confirmez-le.</span><span class="sxs-lookup"><span data-stu-id="93b23-135">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there.</span></span> <span data-ttu-id="93b23-136">Si ce n’est pas le cas, il est possible que vous n’utilisiez pas un pool de réalisateurs.</span><span class="sxs-lookup"><span data-stu-id="93b23-136">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="93b23-137">Si tel est le cas, vous devez utiliser le nom de domaine complet (FQDN) du pool frontal, ou si vous effectuez cette opération pour un serveur unique pour votre serveur Front-End Server ou Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="93b23-137">If that’s the case, you’ll need to use the FQDN of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span>

5.  <span data-ttu-id="93b23-138">Vous devez également vérifier qu’un enregistrement hôte A (AAAA pour IPv6) existe pour votre nom de domaine complet (FQDN) de votre service Web externe (par exemple, lyncwebextpool01.contoso.com), ou un nom de domaine complet pour votre nom de domaine complet (FQDN) de votre serveur principal si vous n’avez pas de pool frontal.</span><span class="sxs-lookup"><span data-stu-id="93b23-138">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or a FQDN for your single-server FQDN if you have no Front End pool.</span></span> <span data-ttu-id="93b23-139">Comme indiqué à l’étape précédente, vous devez disposer de ce qui suit si vous n’avez pas de pool de directeurs.</span><span class="sxs-lookup"><span data-stu-id="93b23-139">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="93b23-140">À présent, dans le format approprié pour votre fournisseur DNS externe, sélectionnez l’option de création d’un **alias (CNAME)** (il s’agit d’une option de menu ou d’un lien, en fonction du format du fournisseur DNS).</span><span class="sxs-lookup"><span data-stu-id="93b23-140">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Alias (CNAME)** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="93b23-141">Il doit exister une forme de zone de texte **nom d’alias** comme le DNS interne, vous devez entrer lyncdiscover comme nom d’hôte de l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="93b23-141">There should be some form of **Alias name** text box as with the internal DNS, you should enter lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="93b23-142">Dans le cas d’un **nom de domaine complet (FQDN)** , vous devez également entrer le nom de domaine complet (FQDN) des services Web externes pour votre pool de directeurs (par exemple, lyncwebexdir01.contoso.com), puis cliquer sur OK ou exécuter une action quelconque du DNS externe pour accepter la création de cette entrée.</span><span class="sxs-lookup"><span data-stu-id="93b23-142">There should also be some form of a **Fully qualified domain name (FQDN) for target host** text box, here’s where you’ll enter the external Web Services FQDN for your Director pool (for example, lyncwebexdir01.contoso.com) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="93b23-143">Comme indiqué à l’étape 4, si vous n’avez pas de pool de directeurs, vous devez utiliser le nom de domaine complet du pool frontal ou le nom de domaine complet (FQDN) du serveur configuré, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="93b23-143">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool FQDN or the single-server FQDN you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="93b23-144">Vous devez créer un nouvel enregistrement CNAMe de découverte automatique dans la zone de recherche directe de chaque domaine SIP pris en charge dans votre environnement Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-144">You’ll need to make a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

</div>

<div>

## <a name="creating-an-internal-dns-a-record"></a><span data-ttu-id="93b23-145">Création d’un enregistrement DNS interne</span><span class="sxs-lookup"><span data-stu-id="93b23-145">Creating an internal DNS A record</span></span>

1.  <span data-ttu-id="93b23-146">Pour créer un enregistrement DNS interne, connectez-vous à un serveur DNS dans votre réseau à l’aide d’un compte de domaine membre du groupe Domain Admins ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="93b23-146">To make an internal DNS record, log on to a DNS server in your network with a domain account that’s a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="93b23-147">Ouvrez le composant logiciel enfichable d’administration DNS : cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="93b23-147">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="93b23-148">Dans le cas d’un enregistrement DNS interne, dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour votre domaine Active Directory (par exemple, contoso. local) sur lequel est installé votre pool de directeurs et votre pool frontal Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-148">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local) where your Lync Server 2013 Director pool and Front End pool are installed.</span></span>

4.  <span data-ttu-id="93b23-149">Pour savoir si un enregistrement hôte A (AAAA pour IPv6) existe pour votre pool de Directors pour un enregistrement DNS interne, un enregistrement A doit exister pour le nom de domaine complet (FQDN) des services Web internes pour votre pool de répertoires (par exemple, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93b23-149">Check and see if a host A (AAAA for IPv6) record exists for your Director pool for an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span> <span data-ttu-id="93b23-150">Si ce n’est pas le cas, il est possible que vous n’utilisiez pas un pool de réalisateurs et que vous deviez utiliser l’adresse IP de votre pool frontal ou même une seule adresse IP de serveur, si c’est votre configuration.</span><span class="sxs-lookup"><span data-stu-id="93b23-150">If it’s not here, you may not be using a Director pool, and you’ll need to use the IP address for your Front End pool or even a single server IP address, if that’s your setup.</span></span>

5.  <span data-ttu-id="93b23-151">Tout en gardant à l’esprit que vous devez vérifier qu’il existe un enregistrement A (AAAA pour IPv6) pour votre pool frontal pour un enregistrement DNS interne, un enregistrement hôte A (ou AAAA) devrait exister pour le nom de domaine complet (FQDN) des services Web internes de votre liste frontale (par exemple, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="93b23-151">Keeping that in mind, check and see if a host A (AAAA for IPv6) record exists for your Front End pool for an internal DNS record, a host A (or AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span> <span data-ttu-id="93b23-152">Si ce n’est pas le cas, vous devez noter l’adresse IP du serveur frontal ou du serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="93b23-152">If it doesn’t, you’ll need to make note of the IP address for the Front End Server or Standard Edition server.</span></span>

6.  <span data-ttu-id="93b23-153">Lorsque vous savez quels sont les enregistrements d’hôte A (ou AAAA), dans l’arborescence de la console de votre serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="93b23-153">Once you know what host A (or AAAA) records exist, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

7.  <span data-ttu-id="93b23-154">Cliquez avec le bouton droit sur le nom de domaine SIP, puis cliquez sur **nouvel hôte (A ou AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="93b23-154">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="93b23-155">Dans **nom**, tapez lyncdiscoverinternal comme nom d’hôte de l’URL du service de découverte automatique interne.</span><span class="sxs-lookup"><span data-stu-id="93b23-155">In **Name**, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="93b23-156">Dans **adresse IP**, tapez l’adresse IP des services Web internes du directeur (ou, si vous utilisez un équilibreur de charge, tapez l’adresse IP virtuelle du directeur de charge).</span><span class="sxs-lookup"><span data-stu-id="93b23-156">In **IP Address**, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span> <span data-ttu-id="93b23-157">Comme indiqué à l’étape 4, si vous n’utilisez pas de réalisateur, il est possible que vous deviez entrer l’adresse IP du serveur frontal ou du serveur Standard Edition ou, si vous utilisez un équilibreur de charge, tapez l’adresse IP de l’équilibrage de charge du pool frontal.</span><span class="sxs-lookup"><span data-stu-id="93b23-157">As noted in Step 4 above, if you aren’t using a Director, you may need to enter the IP address of the Front End Server or Standard Edition server or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

10. <span data-ttu-id="93b23-158">Cliquez sur **Ajouter un hôte**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="93b23-158">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="93b23-159">Pour créer un enregistrement A ou AAAA supplémentaire, répétez les étapes 8 à 10, en gardant à l’esprit que vous devez créer de nouveaux enregistrements de découverte automatique A ou AAAA dans la zone de recherche directe de chaque domaine SIP pris en charge dans votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-159">To create an additional A or AAAA record, repeat steps 8 through 10, keeping in mind that you’ll need to create new Autodiscover A or AAAA records in the forward lookup zone of each SIP domain that’s supported in your Lync Server 2013 environment.</span></span>

12. <span data-ttu-id="93b23-160">Lorsque vous avez terminé de créer un (pour les enregistrements IPv6, AAAA), cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="93b23-160">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

</div>

<div>

## <a name="creating-an-external-dns-a-record"></a><span data-ttu-id="93b23-161">Création d’un enregistrement DNS externe</span><span class="sxs-lookup"><span data-stu-id="93b23-161">Creating an external DNS A record</span></span>

1.  <span data-ttu-id="93b23-162">Pour créer un enregistrement DNS externe, connectez-vous à votre fournisseur DNS public, puis suivez les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="93b23-162">To create an external DNS record, connect to your public DNS provider, and then follow our steps.</span></span> <span data-ttu-id="93b23-163">Nous ne sommes pas en mesure de décrire exactement l’endroit où se trouvent les éléments de l’environnement de votre fournisseur DNS, car il existe peut-être différentes manières de gérer votre DNS externe, mais nous espérons pouvoir suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="93b23-163">We can’t describe exactly where you’re going in your DNS provider’s environment as there may be different ways of managing your external DNS, but we hope these steps help.</span></span>

2.  <span data-ttu-id="93b23-164">Vous devez être connecté en tant que compte qui peut créer des enregistrements DNS dans cet environnement.</span><span class="sxs-lookup"><span data-stu-id="93b23-164">You’ll need to be logged in as an account that can create DNS records in that environment.</span></span>

3.  <span data-ttu-id="93b23-165">Dans le cas d’un enregistrement DNS externe, dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="93b23-165">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span> <span data-ttu-id="93b23-166">Dans le cas d’un enregistrement DNS externe, dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="93b23-166">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="93b23-167">Vous devez déjà voir l’enregistrement d’un hôte A (AAAA pour IPv6) pour votre pool de répertoires (par exemple, lyncwebexdir01.contoso.com), vous devez donc confirmer qu’il est présent et quel est l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="93b23-167">You should already see a host A (AAAA for IPv6) record for your Director pool (such as lyncwebexdir01.contoso.com), so confirm that it’s there and what the IP address is.</span></span> <span data-ttu-id="93b23-168">Si ce n’est pas le cas, il est possible que vous n’utilisiez pas un pool de réalisateurs.</span><span class="sxs-lookup"><span data-stu-id="93b23-168">If it’s not, then you may not be using a Director pool.</span></span> <span data-ttu-id="93b23-169">Si tel est le cas, vous devez utiliser l’adresse IP de votre liste frontale, ou si vous effectuez cette opération pour un serveur unique pour votre serveur Front-End Server ou Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="93b23-169">If that’s the case, you’ll need to use the IP address of your Front End Pool, or if you’re doing this for a single server, for your Front-End server or Standard Edition server.</span></span> <span data-ttu-id="93b23-170">Gardez à l’esprit que vos serveurs sont également situés derrière un équilibreur de charge ou en utilisant un proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="93b23-170">Keep in mind that your servers may also be behind a load-balancer, or using a reverse proxy.</span></span> <span data-ttu-id="93b23-171">Notez également les adresses IP pour pouvoir suivre les étapes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="93b23-171">Make note of the IP addresses as well for following the steps below.</span></span>

5.  <span data-ttu-id="93b23-172">Vous devez également vérifier qu’un enregistrement hôte A (AAAA pour IPv6) existe pour votre nom de domaine complet (FQDN) de votre liste de serveurs Web externes (par exemple, lyncwebextpool01.contoso.com) ou une adresse IP pour votre installation Lync sur un serveur si vous n’avez pas de pool frontal.</span><span class="sxs-lookup"><span data-stu-id="93b23-172">You’ll also need to confirm that a host A (AAAA for IPv6) record exists for your external Web Services Fully Qualified Domain Name (FQDN) for your Front End pool (such as lyncwebextpool01.contoso.com), or an IP address for your single-server Lync installation if you have no Front End pool.</span></span> <span data-ttu-id="93b23-173">Comme indiqué à l’étape précédente, vous devez disposer de ce qui suit si vous n’avez pas de pool de directeurs.</span><span class="sxs-lookup"><span data-stu-id="93b23-173">As noted in the previous step, you’ll need this below if you don’t have a Director pool.</span></span>

6.  <span data-ttu-id="93b23-174">À présent, dans le format approprié pour votre fournisseur DNS externe, choisissez l’option de création d’un **nouvel hôte a ou AAAA** (il s’agit d’une option de menu ou d’un lien, selon le format du fournisseur DNS).</span><span class="sxs-lookup"><span data-stu-id="93b23-174">Now, in the appropriate format for your external DNS provider, choose the option for creating a **New Host A or AAAA** (this may be a menu option or a link, depending on the format of the DNS provider).</span></span>

7.  <span data-ttu-id="93b23-175">Il doit y avoir un lieu pour entrer un **nom**, tapez lyncdiscover comme nom d’hôte de l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="93b23-175">There should be a place to enter a **Name**, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

8.  <span data-ttu-id="93b23-176">Il devrait également y avoir une zone de texte **adresse IP** , vous devez entrer l’adresse IP (par exemple, lyncwebexdir01.contoso.com) ou éventuellement l’adresse IP du système d’équilibrage de charge (ou une adresse IP de proxy inverse), puis cliquer sur OK ou exécuter une action quelconque du DNS externe pour accepter la création de cette entrée.</span><span class="sxs-lookup"><span data-stu-id="93b23-176">There should also be an **IP Address** text box, here’s where you’ll enter the IP for your for your Director pool (for example, lyncwebexdir01.contoso.com) or possibly the IP of your pool’s load balancer (or a reverse proxy IP that leads to the same) and then click OK or take whatever action in the external DNS to accept the creation of this entry.</span></span> <span data-ttu-id="93b23-177">Comme indiqué à l’étape 4, si vous n’avez pas de pool de répertoires, vous devez utiliser l’adresse IP du pool frontal ou l’adresse IP d’un serveur configuré, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="93b23-177">As noted in Step 4, above, if you don’t have a Director pool, you’ll need to use the Front End pool IP address or the single-server IP address you have set up, as appropriate.</span></span>

9.  <span data-ttu-id="93b23-178">Vous devez effectuer une nouvelle découverte automatique A ou un enregistrement AAAA dans la zone de recherche directe de chaque domaine SIP pris en charge dans votre environnement Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="93b23-178">You’ll need to make a new Autodiscover A or AAAA record in the forward lookup zone of each SIP domain that’s supported in your Lync 2013 environment.</span></span>

<span data-ttu-id="93b23-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93b23-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

