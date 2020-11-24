---
title: 'Lync Server 2013 : Configuration des serveurs proxy inverses'
description: 'Lync Server 2013 : configuration de serveurs de proxy inverse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up reverse proxy servers
ms:assetid: 00bc138a-243f-4389-bfa5-9c62fcc95132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398069(v=OCS.15)
ms:contentKeyID: 48183225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8cd5842e4d735637406f6d0fa4f467f1cb8ed03
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394957"
---
# <a name="setting-up-reverse-proxy-servers-for-lync-server-2013"></a><span data-ttu-id="3e91a-103">Configuration des serveurs proxy inverses pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-103">Setting up reverse proxy servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e91a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e91a-104">

<span> </span></span></span>

<span data-ttu-id="3e91a-105">_**Dernière modification de la rubrique :** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="3e91a-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="3e91a-106">Pour les déploiements de serveur Edge Microsoft Lync Server 2013, un proxy HTTPs inverse dans le réseau de périmètre est requis pour que les clients externes accèdent aux services Web de Lync Server 2013 (appelés *composants Web* dans Office Communications Server) sur le directeur et sur le pool d’hébergement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3e91a-106">For Microsoft Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for external clients to access the Lync Server 2013 Web Services (called *Web Components* in Office Communications Server) on the Director and the user’s home pool.</span></span> <span data-ttu-id="3e91a-107">Certaines des fonctionnalités qui nécessitent un accès externe via un proxy inverse sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e91a-107">Some of the features that require external access through a reverse proxy include the following:</span></span>

  - <span data-ttu-id="3e91a-108">Permettre aux utilisateurs externes de télécharger le contenu de la réunion pour vos réunions.</span><span class="sxs-lookup"><span data-stu-id="3e91a-108">Enabling external users to download meeting content for your meetings.</span></span>

  - <span data-ttu-id="3e91a-109">Permettre aux utilisateurs externes d’étendre les groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="3e91a-109">Enabling external users to expand distribution groups.</span></span>

  - <span data-ttu-id="3e91a-110">Permettre aux utilisateurs distants de télécharger des fichiers à partir du service de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3e91a-110">Enabling remote users to download files from the Address Book service.</span></span>

  - <span data-ttu-id="3e91a-111">Accès au client Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="3e91a-111">Accessing the Lync Web App client.</span></span>

  - <span data-ttu-id="3e91a-112">Accès à la page Web des paramètres de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="3e91a-112">Accessing the Dial-in Conferencing Settings webpage.</span></span>

  - <span data-ttu-id="3e91a-113">Permettre aux périphériques externes de se connecter au service Web de mise à jour de l’appareil et d’obtenir les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="3e91a-113">Enabling external devices to connect to Device Update web service and obtain updates.</span></span>

  - <span data-ttu-id="3e91a-114">Activation des applications mobiles pour détecter et utiliser automatiquement les URL de mobilité (MCX) sur Internet.</span><span class="sxs-lookup"><span data-stu-id="3e91a-114">Enabling mobile applications to automatically discover and use the mobility (Mcx) URLs from the Internet.</span></span>

  - <span data-ttu-id="3e91a-115">Activation du client Lync 2013, de l’application Lync du Windows Store et du client mobile Lync 2013 pour trouver les URL de découverte et d’utilisation de l’API Web de communications unifiées (UCWA).</span><span class="sxs-lookup"><span data-stu-id="3e91a-115">Enabling the Lync 2013 client, Lync Windows Store app and Lync 2013 Mobile client to locate the Lync Discover (autodiscover) URLs and use Unified Communications Web API (UCWA).</span></span>

<span data-ttu-id="3e91a-116">Nous vous recommandons de configurer votre proxy HTTP inverse pour publier tous les services Web dans tous les groupes.</span><span class="sxs-lookup"><span data-stu-id="3e91a-116">We recommend that you configure your HTTP reverse proxy to publish all Web Services in all pools.</span></span> <span data-ttu-id="3e91a-117">Publication de https://ExternalFQDN/ \* publie tous les répertoires virtuels IIS d’un pool.</span><span class="sxs-lookup"><span data-stu-id="3e91a-117">Publishing https:// ExternalFQDN/\* publishes all IIS virtual directories for a pool.</span></span> <span data-ttu-id="3e91a-118">Vous avez besoin d’une seule règle de publication pour chaque serveur Standard Edition, pool frontal ou pool ou pool de réalisateur au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3e91a-118">You need one publishing rule for each Standard Edition server, Front End pool, or Director or Director pool in your organization.</span></span>

<span data-ttu-id="3e91a-119">Par ailleurs, vous devez publier les URL simples.</span><span class="sxs-lookup"><span data-stu-id="3e91a-119">In addition, you need to publish the simple URLs.</span></span> <span data-ttu-id="3e91a-120">Si votre organisation dispose d’un directeur ou d’un pool de directeurs, le proxy HTTP inverse écoute les requêtes HTTP/HTTPs aux URL simples et aux proxys vers le répertoire virtuel des services Web externes du réalisateur ou du pool de réalisateurs.</span><span class="sxs-lookup"><span data-stu-id="3e91a-120">If the organization has a Director or Director pool, the HTTP reverse proxy listens for HTTP/HTTPS requests to the simple URLs and proxies them to the external Web Services virtual directory on the Director or Director pool.</span></span> <span data-ttu-id="3e91a-121">Si vous n’avez pas déployé de réalisateur, vous devez désigner un pool pour gérer les requêtes aux URL simples.</span><span class="sxs-lookup"><span data-stu-id="3e91a-121">If you have not deployed a Director, you need to designate one pool to handle requests to the simple URLs.</span></span> <span data-ttu-id="3e91a-122">(S’il ne s’agit pas de la liste de ressources partagées de l’utilisateur, celui-ci est redirigé vers les services Web sur le pool de ressources de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="3e91a-122">(If this is not the user’s home pool, it will redirect them onward to the Web Services on the user’s home pool).</span></span> <span data-ttu-id="3e91a-123">Les URL simples peuvent être gérées par une règle de publication Web dédiée ou ajoutées au nom public de la règle de publication Web pour le directeur.</span><span class="sxs-lookup"><span data-stu-id="3e91a-123">The simple URLs can be handled by a dedicated web publishing rule, or you can add it to the public names of the web publishing rule for the Director.</span></span> <span data-ttu-id="3e91a-124">Vous devez également publier l’URL du service de découverte automatique externe.</span><span class="sxs-lookup"><span data-stu-id="3e91a-124">You also need to publish the external Autodiscover Service URL.</span></span>

<span data-ttu-id="3e91a-125">Vous pouvez utiliser Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1 ou Internet Information Server 7,0, 7,5 ou 8,0 avec le routage de requête d’application (IIS ARR) en tant que proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="3e91a-125">You can use Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, or Internet Information Server 7.0, 7.5 or 8.0 with Application Request Routing (IIS ARR) as a reverse proxy.</span></span> <span data-ttu-id="3e91a-126">Les étapes décrites dans cette section décrivent la configuration de la passerelle de gestion des menaces de gestion de la 2010 et les étapes de configuration d’ISA Server 2006 sont presque identiques.</span><span class="sxs-lookup"><span data-stu-id="3e91a-126">The detailed steps in this section describe how to configure Forefront Threat Management Gateway 2010, and the steps for configuring ISA Server 2006 are almost identical.</span></span> <span data-ttu-id="3e91a-127">Des instructions sont également fournies pour IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="3e91a-127">Guidance is also provided for IIS ARR.</span></span> <span data-ttu-id="3e91a-128">Si vous utilisez un proxy inverse différent, consultez la documentation de ce produit et mappez les exigences définies ici aux fonctionnalités associées dans d’autres proxys inverse.</span><span class="sxs-lookup"><span data-stu-id="3e91a-128">If you are using a different reverse proxy, consult the documentation for that product and map the requirements defined here to the associated features in other reverse proxies.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3e91a-129">Le routage de requête d’application Internet Information Server (IIS ARR) est une option entièrement testée et prise en charge permettant d’implémenter un proxy inverse pour Lync Server 2010 et Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3e91a-129">Internet Information Server Application Request Routing (IIS ARR) is a fully tested and supported option for implementing a reverse proxy for Lync Server 2010 and Lync Server 2013.</span></span> <span data-ttu-id="3e91a-130">En novembre, 2012, Microsoft a cessé de gérer les licences de ForeFront Threat Management Gateway 2010 ou TMG.</span><span class="sxs-lookup"><span data-stu-id="3e91a-130">In November, 2012, Microsoft ceased license sales of ForeFront Threat Management Gateway 2010, or TMG.</span></span> <span data-ttu-id="3e91a-131">TMG est toujours un produit entièrement pris en charge et est toujours disponible à la vente sur des appareils vendus par des tiers.</span><span class="sxs-lookup"><span data-stu-id="3e91a-131">TMG is still a fully supported product, and is still available for sale on appliances sold by third parties.</span></span> <span data-ttu-id="3e91a-132">De plus, de nombreux équilibreurs de charge matérielle tiers et de pare-feu fournissent la prise en charge du proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="3e91a-132">Also, many third party hardware load balancers and firewalls provide reverse proxy support.</span></span> <span data-ttu-id="3e91a-133">Pour les dispositifs d’équilibrage de charge matérielle et de pare-feu qui fournissent des fonctionnalités de proxy inverse, contactez votre fabricant pour obtenir des instructions spécifiques sur la configuration de ses produits pour la prise en charge du proxy inverse de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3e91a-133">For hardware load balancers and firewalls that provide reverse proxy features, check with your vendor for specific instructions on how to configure their product to provide reverse proxy support for Lync Server.</span></span> <span data-ttu-id="3e91a-134">Vous pouvez également afficher des parties tierces ayant soumis une documentation pour leur produit à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e91a-134">You can also view third parties that have submitted documentation for their product to Microsoft.</span></span> <span data-ttu-id="3e91a-135">La prise en charge est assurée par le tiers pour sa solution.</span><span class="sxs-lookup"><span data-stu-id="3e91a-135">Support is provided by the third party for their solution.</span></span> <span data-ttu-id="3e91a-136">Pour voir d’autres parties actives dans la fourniture de solutions, voir <A href="https://go.microsoft.com/fwlink/?linkid=268730">infrastructure Qualified pour Microsoft Lync</A>.</span><span class="sxs-lookup"><span data-stu-id="3e91a-136">To see third parties that are active in providing solutions, see <A href="https://go.microsoft.com/fwlink/?linkid=268730">Infrastructure qualified for Microsoft Lync</A>.</span></span>



</div>

<span data-ttu-id="3e91a-137">Les rubriques et procédures suivantes utilisent Forefront Threat Management Gateway 2010 et IIS ARR comme base pour les procédures de déploiement et de configuration.</span><span class="sxs-lookup"><span data-stu-id="3e91a-137">The following topics and procedures use Forefront Threat Management Gateway 2010 and IIS ARR as the basis for the deployment and configuration procedures.</span></span>

  - [<span data-ttu-id="3e91a-138">Configuration des noms de domaine complets d’une batterie de serveurs web pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-138">Configure web farm FQDNs for Lync Server 2013</span></span>](lync-server-2013-configure-web-farm-fqdns.md)

  - [<span data-ttu-id="3e91a-139">Configuration des cartes réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-139">Configure network adapters in Lync Server 2013</span></span>](lync-server-2013-configure-network-adapters.md)

  - [<span data-ttu-id="3e91a-140">Demande et configuration d’un certificat pour votre proxy HTTP inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-140">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md)

  - [<span data-ttu-id="3e91a-141">Configuration des règles de publication web pour un pool interne unique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-141">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>](lync-server-2013-configure-web-publishing-rules-for-a-single-internal-pool.md)

  - [<span data-ttu-id="3e91a-142">Connexion d’un Survivable Branch Appliance à un pool de serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="3e91a-142">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>](lync-server-2013-verify-or-configure-authentication-and-certification-on-iis-virtual-directories.md)

  - [<span data-ttu-id="3e91a-143">Création des enregistrements DNS pour les serveurs proxy inverses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-143">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)

  - [<span data-ttu-id="3e91a-144">Vérification de l’accès avec le proxy inverse dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e91a-144">Verify access through your reverse proxy in Lync Server 2013</span></span>](lync-server-2013-verify-access-through-your-reverse-proxy.md)

<div>

## <a name="before-you-begin"></a><span data-ttu-id="3e91a-145">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3e91a-145">Before You Begin</span></span>

<span data-ttu-id="3e91a-146">Pour réussir le déploiement de Forefront Threat Management Gateway 2010 en tant que proxy inverse, vous devez configurer et configurer un serveur en utilisant la configuration requise et la configuration matérielle requise définie dans la documentation de la 2010 passerelle de gestion des menaces de Forefront.</span><span class="sxs-lookup"><span data-stu-id="3e91a-146">To successfully deploy Forefront Threat Management Gateway 2010 as your reverse proxy, you need to setup and configure a server, using the prerequisites and hardware requirements defined in the Forefront Threat Management Gateway 2010 documentation.</span></span> <span data-ttu-id="3e91a-147">Pour plus d’informations, reportez-vous à la rubrique suivante configurée pour configurer correctement le matériel et installer la passerelle 2010 de Forefront Threat Management sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="3e91a-147">See the following topic set to properly configure the hardware and to install Forefront Threat Management Gateway 2010 on the server before proceeding.</span></span>

  - <span></span>  
    [<span data-ttu-id="3e91a-148">Passerelle de gestion des menaces de Forefront (TMG) 2010</span><span class="sxs-lookup"><span data-stu-id="3e91a-148">Forefront Threat Management Gateway (TMG) 2010</span></span>](https://go.microsoft.com/fwlink/?linkid=291292)

  - <span></span>  
    [<span data-ttu-id="3e91a-149">Recommandations en matière de matériel de Forefront TMG 2010</span><span class="sxs-lookup"><span data-stu-id="3e91a-149">Forefront TMG 2010 hardware recommendations</span></span>](https://go.microsoft.com/fwlink/?linkid=291293)

<span data-ttu-id="3e91a-150">Pour déployer correctement IIS ARR en tant que proxy inverse, consultez les rubriques suivantes pour configurer le matériel et les logiciels requis.</span><span class="sxs-lookup"><span data-stu-id="3e91a-150">To successfully deploy IIS ARR as your reverse proxy, review the following topics to configure the hardware and the prerequisite software.</span></span>

  - <span></span>  
    <span data-ttu-id="3e91a-151">Pour installer IIS sur Windows Server 2008 ou Windows Server 2008 R2, voir [installer IIS 7 sur Windows server 2008 ou Windows server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296) .</span><span class="sxs-lookup"><span data-stu-id="3e91a-151">To install IIS on Windows Server 2008 or Windows Server 2008 R2, see [Installing IIS 7 on Windows Server 2008 or Windows Server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span></span>

  - <span></span>  
    <span data-ttu-id="3e91a-152">Pour installer IIS sur Windows Server 2012, voir [installer IIS 8 sur Windows server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span><span class="sxs-lookup"><span data-stu-id="3e91a-152">To install IIS on Windows Server 2012, see [Installing IIS 8 on Windows Server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span></span>

  - <span></span>  
    <span data-ttu-id="3e91a-153">Pour installer IIS sur Windows Server 2012 R2, voir [installer iis 8,5 sur Windows server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687) .</span><span class="sxs-lookup"><span data-stu-id="3e91a-153">To install IIS on Windows Server 2012 R2, see [Installing IIS 8.5 on Windows Server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span></span>

  - <span></span>  
    <span data-ttu-id="3e91a-154">Pour télécharger l’extension de routage de requête d’application pour les services Internet (IIS), suivez les instructions de téléchargement de l’application requête de routage [v 2,5](https://go.microsoft.com/fwlink/?linkid=291298) .</span><span class="sxs-lookup"><span data-stu-id="3e91a-154">To download the Application Request Routing extension for IIS, follow the instructions at [Application Request Routing v2.5 Download](https://go.microsoft.com/fwlink/?linkid=291298)</span></span>

  - <span></span>  
    <span data-ttu-id="3e91a-155">Pour installer l’application ARR, pour les instructions de la procédure d’installation de l' [application demande de routage version 2](https://go.microsoft.com/fwlink/?linkid=291299)</span><span class="sxs-lookup"><span data-stu-id="3e91a-155">To install ARR, for the instructions at [Install Application Request Routing Version 2](https://go.microsoft.com/fwlink/?linkid=291299)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3e91a-156">Les instructions actuellement publiées sont pour ARR 2,0.</span><span class="sxs-lookup"><span data-stu-id="3e91a-156">The instructions currently posted are for ARR 2.0.</span></span> <span data-ttu-id="3e91a-157">Pour l’installation de l’extension, il n’y a pas de différence entre les deux versions.</span><span class="sxs-lookup"><span data-stu-id="3e91a-157">For installation of the extension, there is no difference between the two versions.</span></span>

    
    <span data-ttu-id="3e91a-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e91a-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

