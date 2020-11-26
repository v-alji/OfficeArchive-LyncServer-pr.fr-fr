---
title: 'Lync Server 2013 : configuration du DNS pour la découverte automatique'
description: 'Lync Server 2013 : configuration du DNS pour la découverte automatique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring DNS for Autodiscover
ms:assetid: f07a634c-3cf3-4958-8556-84596319ef54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945656(v=OCS.15)
ms:contentKeyID: 51541528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98a56cf3aa260bcbec9099e65958a9b17c3eaf26
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433184"
---
# <a name="configuring-dns-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="e9559-103">Configuration de DNS pour la découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9559-103">Configuring DNS for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9559-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9559-104">

<span> </span></span></span>

<span data-ttu-id="e9559-105">_**Dernière modification de la rubrique :** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="e9559-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="e9559-106">Pour prendre en charge la découverte automatique pour les clients Lync, vous devez créer les enregistrements DNS suivants :</span><span class="sxs-lookup"><span data-stu-id="e9559-106">To support autodiscovery for Lync clients, you need to create the following Domain Name System (DNS) records:</span></span>

  - <span data-ttu-id="e9559-107">Un enregistrement DNS interne pour la prise en charge des clients Lync qui se connectent au sein du réseau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e9559-107">An internal DNS record to support Lync clients who connect from within your organization's network</span></span>

  - <span data-ttu-id="e9559-108">Enregistrement DNS externe ou public permettant de prendre en charge les clients Lync qui se connectent à partir d’Internet</span><span class="sxs-lookup"><span data-stu-id="e9559-108">An external, or public, DNS record to support Lync clients who connect from the Internet</span></span>

<span data-ttu-id="e9559-109">Vous devez créer un enregistrement DNS interne et un enregistrement DNS externe pour chaque domaine SIP.</span><span class="sxs-lookup"><span data-stu-id="e9559-109">You must create an internal DNS record and an external DNS record for each SIP domain.</span></span>

<span data-ttu-id="e9559-110">Les enregistrements DNS peuvent être des enregistrements CNAMe ou CNAMe, en fonction de votre capacité à créer des certificats avec le nouveau nom d’objet.</span><span class="sxs-lookup"><span data-stu-id="e9559-110">The DNS records can be either A (host) records or CNAME records, based on your ability to create new certificates with the additional subject alternate name (SAN).</span></span> <span data-ttu-id="e9559-111">Si vous n’êtes pas en mesure de demander et de déployer un nouveau certificat externe (public) avec le lyncdiscover.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="e9559-111">If you are not able to request and deploy a new external (public) certificate with the lyncdiscover.\<domain name\></span></span> <span data-ttu-id="e9559-112">Utilisez la procédure d’utilisation de la 80 port TCP/TCP.</span><span class="sxs-lookup"><span data-stu-id="e9559-112">SAN, use the procedure for using HTTP/TCP port 80.</span></span> <span data-ttu-id="e9559-113">Les procédures suivantes décrivent la création d’enregistrements DNS internes et externes.</span><span class="sxs-lookup"><span data-stu-id="e9559-113">The following procedures describe how to create internal and external DNS records.</span></span>

<div>

## <a name="to-create-dns-cname-records"></a><span data-ttu-id="e9559-114">Pour créer des enregistrements CNAMe DNS</span><span class="sxs-lookup"><span data-stu-id="e9559-114">To create DNS CNAME records</span></span>

1.  <span data-ttu-id="e9559-115">Connectez-vous à un serveur DNS comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-115">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="e9559-116">Pour créer un enregistrement DNS interne, connectez-vous à un serveur DNS de votre réseau en tant que membre du groupe Domain Admins ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="e9559-116">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="e9559-117">Pour créer un enregistrement DNS externe, connectez-vous à votre fournisseur DNS public.</span><span class="sxs-lookup"><span data-stu-id="e9559-117">To create an external DNS record, connect to your public DNS provider.</span></span>

2.  <span data-ttu-id="e9559-118">Ouvrez le composant logiciel enfichable d’administration DNS : cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="e9559-118">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="e9559-119">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9559-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="e9559-120">Pour un enregistrement DNS interne, dans l’arborescence de la console du serveur DNS, développez la **zone de recherche directe** pour votre domaine Active Directory (par exemple, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-120">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e9559-121">Ce domaine est le domaine Active Directory dans lequel votre &nbsp; pool de directeurs Lync Server 2013 et votre pool frontal sont installés.</span><span class="sxs-lookup"><span data-stu-id="e9559-121">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="e9559-122">Dans le cas d’un enregistrement DNS externe, dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-122">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="e9559-123">Vérifiez qu’un enregistrement A existe pour votre pool de directeurs comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-123">Verify that a host A record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="e9559-124">Dans le cas d’un enregistrement DNS interne, un enregistrement A doit exister pour le nom de domaine complet (FQDN) des services Web internes pour votre pool de répertoires (par exemple, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-124">For an internal DNS record, a host A record should exist for the internal Web Services fully qualified domain name (FQDN) for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="e9559-125">Dans le cas d’un enregistrement DNS externe, un enregistrement de l’hôte A doit exister pour le nom de domaine complet des services Web externes de votre pool de directeurs (par exemple, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-125">For an external DNS record, a host A record should exist for the external web services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="e9559-126">Vérifiez qu’un enregistrement A existe pour votre pool frontal comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-126">Verify that a host A record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="e9559-127">Dans le cas d’un enregistrement DNS interne, un enregistrement A doit exister pour le nom de domaine complet des services Web internes de votre pool frontal (par exemple, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-127">For an internal DNS record, a host A record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="e9559-128">Dans le cas d’un enregistrement DNS externe, un enregistrement de l’hôte A doit exister pour le nom de domaine complet des services Web externes de votre pool frontal (par exemple, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-128">For an external DNS record, a host A record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="e9559-129">Pour un enregistrement DNS interne, dans l’arborescence de la console de votre serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-129">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9559-130">Si vous créez un enregistrement DNS externe, les <STRONG>zones de recherche directe</STRONG> sont déjà développées pour votre domaine SIP à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="e9559-130">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="e9559-131">Cliquez avec le bouton droit sur le nom de domaine SIP, puis cliquez sur **Nouvel alias (CNAME)**.</span><span class="sxs-lookup"><span data-stu-id="e9559-131">Right-click the SIP domain name, and then click **New Alias (CNAME)**.</span></span>

8.  <span data-ttu-id="e9559-132">Dans **nom** de l’alias, tapez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9559-132">In **Alias name**, type one of the following:</span></span>
    
      - <span data-ttu-id="e9559-133">Pour un enregistrement DNS interne, tapez lyncdiscoverinternal comme nom d’hôte de l’URL du service de découverte automatique interne.</span><span class="sxs-lookup"><span data-stu-id="e9559-133">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="e9559-134">Pour un enregistrement DNS externe, tapez lyncdiscover comme nom d’hôte de l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="e9559-134">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>

9.  <span data-ttu-id="e9559-135">Dans **nom de domaine complet (FQDN) de l’hôte cible**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9559-135">In **Fully qualified domain name (FQDN) for target host**, do one of the following:</span></span>
    
      - <span data-ttu-id="e9559-136">Pour un enregistrement DNS interne, tapez ou accédez au nom de domaine complet des services Web internes de votre pool de réalisateurs (par exemple, lyncwebdir01. contoso. local), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9559-136">For an internal DNS record, type or browse to the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local), and then click **OK**.</span></span>
    
      - <span data-ttu-id="e9559-137">Pour un enregistrement DNS externe, tapez ou accédez au nom de domaine complet des services Web externes de votre pool de réalisateurs (par exemple, lyncwebextdir.contoso.com), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9559-137">For an external DNS record, type or browse to the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9559-138">Si vous n’utilisez pas de réalisateur, utilisez le nom de domaine complet (FQDN) de services Web interne et externe pour le pool frontal, ou, pour un serveur unique, le nom de domaine complet (FQDN) du serveur frontal ou du serveur Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="e9559-138">If you do not use a Director, use the internal and external Web Services FQDN for the Front End pool, or, for a single server, the FQDN for the Front End Server or Standard Edition server.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e9559-139">Vous devez créer un enregistrement CNAMe de découverte automatique dans la zone de recherche directe de chaque domaine SIP que vous prenez en charge dans votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e9559-139">You must create a new Autodiscover CNAME record in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

</div>

<div>

## <a name="to-create-dns-a-records"></a><span data-ttu-id="e9559-140">Pour créer des enregistrements DNS A</span><span class="sxs-lookup"><span data-stu-id="e9559-140">To create DNS A records</span></span>

1.  <span data-ttu-id="e9559-141">Connectez-vous à un serveur DNS comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-141">Log on to a DNS server as follows:</span></span>
    
      - <span data-ttu-id="e9559-142">Pour créer un enregistrement DNS interne, connectez-vous à un serveur DNS de votre réseau en tant que membre du groupe Domain Admins ou membre du groupe DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="e9559-142">To create an internal DNS record, log on to a DNS server in your network as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>
    
      - <span data-ttu-id="e9559-143">Pour créer un enregistrement DNS externe, connectez-vous à votre fournisseur DNS public ou votre serveur DNS externe.</span><span class="sxs-lookup"><span data-stu-id="e9559-143">To create an external DNS record, connect to your public DNS provider or external DNS server.</span></span>

2.  <span data-ttu-id="e9559-144">Ouvrez le composant logiciel enfichable d’administration DNS : cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **DNS**.</span><span class="sxs-lookup"><span data-stu-id="e9559-144">Open the DNS administrative snap-in: Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="e9559-145">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e9559-145">Do one of the following:</span></span>
    
      - <span data-ttu-id="e9559-146">Pour un enregistrement DNS interne, dans l’arborescence de la console du serveur DNS, développez la **zone de recherche directe** pour votre domaine Active Directory (par exemple, contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-146">For an internal DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your Active Directory domain (for example, contoso.local).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e9559-147">Ce domaine est le domaine Active Directory dans lequel votre &nbsp; pool de directeurs Lync Server 2013 et votre pool frontal sont installés.</span><span class="sxs-lookup"><span data-stu-id="e9559-147">This domain is the Active Directory domain where your Lync Server 2013&nbsp;Director pool and Front End pool are installed.</span></span>

        
        </div>
    
      - <span data-ttu-id="e9559-148">Dans le cas d’un enregistrement DNS externe, dans l’arborescence de la console du serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-148">For an external DNS record, in the console tree of the DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>

4.  <span data-ttu-id="e9559-149">Vérifiez qu’un enregistrement hôte A (pour IPv6, AAAA) existe pour votre pool de réalisateurs comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-149">Verify that a host A (for IPv6, AAAA) record exists for your Director pool as follows:</span></span>
    
      - <span data-ttu-id="e9559-150">Dans le cas d’un enregistrement DNS interne, un enregistrement hôte A (pour IPv6, AAAA) doit exister pour le nom de domaine complet (FQDN) des services Web internes de votre pool de directeurs (par exemple, lyncwebdir01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-150">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Director pool (for example, lyncwebdir01.contoso.local).</span></span>
    
      - <span data-ttu-id="e9559-151">Dans le cas d’un enregistrement DNS externe, un enregistrement hôte A (pour IPv6, AAAA) doit exister pour le nom de domaine complet des services Web externes de votre pool de directeurs (par exemple, lyncwebextdir.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-151">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Director pool (for example, lyncwebextdir.contoso.com).</span></span>

5.  <span data-ttu-id="e9559-152">Vérifiez qu’un enregistrement A (pour IPv6, AAAA) existe pour le pool frontal comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-152">Verify that a host A (for IPv6, AAAA) record exists for your Front End pool as follows:</span></span>
    
      - <span data-ttu-id="e9559-153">Dans le cas d’un enregistrement DNS interne, un enregistrement hôte A (pour IPv6, AAAA) doit exister pour le nom de domaine complet des services Web internes de votre pool frontal (par exemple, lyncwebpool01. contoso. local).</span><span class="sxs-lookup"><span data-stu-id="e9559-153">For an internal DNS record, a host A (for IPv6, AAAA) record should exist for the internal Web Services FQDN for your Front End pool (for example, lyncwebpool01.contoso.local).</span></span>
    
      - <span data-ttu-id="e9559-154">Dans le cas d’un enregistrement DNS externe, un enregistrement hôte A (pour IPv6, AAAA) doit exister pour le nom de domaine complet des services Web externes de votre pool frontal (par exemple, lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-154">For an external DNS record, a host A (for IPv6, AAAA) record should exist for the external Web Services FQDN for your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>

6.  <span data-ttu-id="e9559-155">Pour un enregistrement DNS interne, dans l’arborescence de la console de votre serveur DNS, développez **zones de recherche directe** pour votre domaine SIP (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="e9559-155">For an internal DNS record, in the console tree of your DNS server, expand **Forward Lookup Zones** for your SIP domain (for example, contoso.com).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9559-156">Si vous créez un enregistrement DNS externe, les <STRONG>zones de recherche directe</STRONG> sont déjà développées pour votre domaine SIP à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="e9559-156">If you are creating an external DNS record, <STRONG>Forward Lookup Zones</STRONG> is already expanded for your SIP domain from step 3.</span></span>

    
    </div>

7.  <span data-ttu-id="e9559-157">Cliquez avec le bouton droit sur le nom de domaine SIP, puis cliquez sur **nouvel hôte (A ou AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="e9559-157">Right-click the SIP domain name, and then click **New Host (A or AAAA)**.</span></span>

8.  <span data-ttu-id="e9559-158">Dans **nom**, tapez le nom d’hôte comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-158">In **Name**, type the host name as follows:</span></span>
    
      - <span data-ttu-id="e9559-159">Pour un enregistrement DNS interne, tapez lyncdiscoverinternal comme nom d’hôte de l’URL du service de découverte automatique interne.</span><span class="sxs-lookup"><span data-stu-id="e9559-159">For an internal DNS record, type lyncdiscoverinternal as the host name for the internal Autodiscover Service URL.</span></span>
    
      - <span data-ttu-id="e9559-160">Pour un enregistrement DNS externe, tapez lyncdiscover comme nom d’hôte de l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="e9559-160">For an external DNS record, type lyncdiscover as the host name for the external Autodiscover Service URL.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9559-161">Le nom de domaine est supposé à partir de la zone dans laquelle l’enregistrement est défini et, par conséquent, n’a pas besoin d’être entré dans le cadre de l’enregistrement A.</span><span class="sxs-lookup"><span data-stu-id="e9559-161">The domain name is assumed from the zone in which the record is defined and, therefore, does not need to be entered as part of the A record.</span></span>

    
    </div>

9.  <span data-ttu-id="e9559-162">Dans **adresse IP**, tapez l’adresse IP comme suit :</span><span class="sxs-lookup"><span data-stu-id="e9559-162">In **IP Address**, type the IP address as follows:</span></span>
    
      - <span data-ttu-id="e9559-163">Dans le cas d’un enregistrement DNS interne, tapez l’adresse IP de services Web internes du directeur (ou, si vous utilisez un équilibreur de charge, tapez l’adresse IP virtuelle de l’équilibreur de charge).</span><span class="sxs-lookup"><span data-stu-id="e9559-163">For an internal DNS record, type the internal Web Services IP address of the Director (or, if you use a load balancer, type the virtual IP (VIP) of the Director load balancer).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="e9559-164">Si vous n’utilisez pas de réalisateur, tapez l’adresse IP du serveur frontal ou du serveur Standard Edition, ou, si vous utilisez un équilibreur de charge, tapez l’adresse IP du serveur principal de chargement.</span><span class="sxs-lookup"><span data-stu-id="e9559-164">If you do not use a Director, type the IP address of the Front End Server or Standard Edition server, or, if you use a load balancer, type the VIP of the Front End pool load balancer.</span></span>

        
        </div>
    
      - <span data-ttu-id="e9559-165">Pour un enregistrement DNS externe, tapez l’adresse IP externe ou publique du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="e9559-165">For an external DNS record, type the external or public IP address of the reverse proxy.</span></span>

10. <span data-ttu-id="e9559-166">Cliquez sur **Ajouter un hôte**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9559-166">Click **Add Host**, and then click **OK**.</span></span>

11. <span data-ttu-id="e9559-167">Pour créer un enregistrement A supplémentaires, répétez les étapes 8 à 10.</span><span class="sxs-lookup"><span data-stu-id="e9559-167">To create an additional A record, repeat steps 8 through 10.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e9559-168">Vous devez créer un nouveau lyncdiscover et lyncdiscoverinternal A enregistrements dans la zone de recherche directe de chaque domaine SIP que vous prenez en charge dans votre environnement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e9559-168">You must create a new lyncdiscover and lyncdiscoverinternal A records in the forward lookup zone of each SIP domain that you support in your Lync Server 2013 environment.</span></span>

    
    </div>

12. <span data-ttu-id="e9559-169">Lorsque vous avez terminé de créer un (pour les enregistrements IPv6, AAAA), cliquez sur **terminé**.</span><span class="sxs-lookup"><span data-stu-id="e9559-169">When you are finished creating A (for IPv6, AAAA) records, click **Done**.</span></span>

<span data-ttu-id="e9559-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9559-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

