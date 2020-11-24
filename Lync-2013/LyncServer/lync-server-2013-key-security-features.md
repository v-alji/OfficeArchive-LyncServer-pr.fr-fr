---
title: 'Lync Server 2013 : principales fonctionnalités de sécurité'
description: 'Lync Server 2013 : principales fonctionnalités de sécurité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Key security features in Lync Server 2013
ms:assetid: bf2a3b8f-73c6-47e1-8c9e-ca1dc1a502bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342829(v=OCS.15)
ms:contentKeyID: 56107266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 689cf2ac54eacd24bb4d31b451836edcf676521b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394360"
---
# <a name="key-security-features-in-lync-server-2013"></a><span data-ttu-id="800ae-103">Principales fonctionnalités de sécurité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="800ae-103">Key security features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="800ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="800ae-104">

<span> </span></span></span>

<span data-ttu-id="800ae-105">_**Dernière modification de la rubrique :** 2013-07-18_</span><span class="sxs-lookup"><span data-stu-id="800ae-105">_**Topic Last Modified:** 2013-07-18_</span></span>

<span data-ttu-id="800ae-106">Lync Server 2013 inclut plusieurs fonctionnalités de sécurité, notamment l’authentification de serveur à serveur, le contrôle d’accès basé sur un rôle et le stockage centralisé des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="800ae-106">Lync Server 2013 includes several security features, including server-to-server authentication, role-based access control, and centralized storage of configuration data.</span></span>

<span data-ttu-id="800ae-107">Cet article fournit une vue d’ensemble de haut niveau de la sécurité de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="800ae-107">This article provides a high level overview of Lync Server 2013 security.</span></span>

<div>

## <a name="key-security-features-in-lync-server-2013"></a><span data-ttu-id="800ae-108">Principales fonctionnalités de sécurité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="800ae-108">Key Security Features in Lync Server 2013</span></span>

<span data-ttu-id="800ae-109">La sécurité est un sujet très large.</span><span class="sxs-lookup"><span data-stu-id="800ae-109">Security is a very broad topic.</span></span> <span data-ttu-id="800ae-110">La sécurité s’étend à toutes les fonctionnalités de Lync Server 2013 ainsi qu’aux bases de données, services et matériels qui constituent un écosystème Lync.</span><span class="sxs-lookup"><span data-stu-id="800ae-110">Security reaches across every feature of Lync Server 2013 as well as databases, services, and hardware that make up a Lync ecosystem.</span></span> <span data-ttu-id="800ae-111">Cet article présente certaines des fonctionnalités de Lync Server 2013 en particulier qui sont conçues pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="800ae-111">This article outlines some of the features in Lync Server 2013 in particular that are designed for security.</span></span>

<div>

## <a name="planning-and-design-tools"></a><span data-ttu-id="800ae-112">Outils de planification et de conception</span><span class="sxs-lookup"><span data-stu-id="800ae-112">Planning and Design Tools</span></span>

<span data-ttu-id="800ae-113">Lync Server 2013 fournit deux outils pour faciliter la planification et la conception, et limiter les risques de configuration des composants serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="800ae-113">Lync Server 2013 provides two tools to facilitate planning and design and to reduce the chance of misconfiguring Lync Server components.</span></span>

  - <span data-ttu-id="800ae-114">L' **outil de planification topologique** automatise une grande partie du processus de conception topologique.</span><span class="sxs-lookup"><span data-stu-id="800ae-114">**Topology Planning Tool** automates much of the topology design process.</span></span> <span data-ttu-id="800ae-115">Vous pouvez exporter les résultats de l’outil de planification au générateur de topologie, qui est l’outil requis pour installer chaque serveur exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="800ae-115">You can export the results from the Planning Tool to Topology Builder, which is the tool that is required to install each server running Lync Server 2013.</span></span>

  - <span data-ttu-id="800ae-116">**Le générateur de topologie** stocke toutes les informations de configuration dans le magasin central de gestion.</span><span class="sxs-lookup"><span data-stu-id="800ae-116">**Topology Builder** stores all configuration information in the Central Management store.</span></span>

<span data-ttu-id="800ae-117">Pour plus d’informations sur ces outils, voir [planification de Lync Server 2013](lync-server-2013-planning.md).</span><span class="sxs-lookup"><span data-stu-id="800ae-117">For details about these tools, see [Planning for Lync Server 2013](lync-server-2013-planning.md).</span></span>

</div>

<div>

## <a name="central-management-store"></a><span data-ttu-id="800ae-118">Magasin central de gestion</span><span class="sxs-lookup"><span data-stu-id="800ae-118">Central Management Store</span></span>

<span data-ttu-id="800ae-119">Dans Lync Server 2013, les données de configuration relatives aux serveurs et services font partie du magasin central de gestion.</span><span class="sxs-lookup"><span data-stu-id="800ae-119">In Lync Server 2013, configuration data about servers and services is part of the Central Management store.</span></span> <span data-ttu-id="800ae-120">Le centre de gestion central fournit un stockage puissant et schematized des données nécessaires pour définir, configurer, gérer, gérer, décrire et utiliser un déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="800ae-120">The Central Management store provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync Server deployment.</span></span> <span data-ttu-id="800ae-121">Il valide également les données afin de garantir la cohérence de la configuration.</span><span class="sxs-lookup"><span data-stu-id="800ae-121">It also validates the data to ensure configuration consistency.</span></span> <span data-ttu-id="800ae-122">Toutes les modifications apportées aux données de configuration ont lieu dans le magasin central de gestion, ce qui élimine les problèmes de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="800ae-122">All changes to this configuration data happen at the Central Management store, eliminating “out-of-sync” issues.</span></span>

<span data-ttu-id="800ae-p104">Les copies en lecture seule des données sont répliquées sur tous les serveurs au sein de la topologie, y compris les serveurs Edge et les serveurs Survivable Branch Appliance. La réplication est gérée par un service exécuté par défaut dans le contexte du service réseau, ce qui limite les droits et autorisations à ceux d’un simple utilisateur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="800ae-p104">Read-only copies of the data are replicated to all servers in the topology, including Edge Servers and Survivable Branch Appliances. Replication is managed by a service that is, by default, run under the context of the Network service, reducing the rights and permissions to that of a simple user on the computer.</span></span>

</div>

<div>

## <a name="server-to-server-authentication"></a><span data-ttu-id="800ae-125">Authentification serveur à serveur</span><span class="sxs-lookup"><span data-stu-id="800ae-125">Server-to-Server Authentication</span></span>

<span data-ttu-id="800ae-126">Dans Lync Server 2013, il est possible de configurer l’authentification entre les serveurs à l’aide du protocole d’autorisation Open (OAuth).</span><span class="sxs-lookup"><span data-stu-id="800ae-126">In Lync Server 2013, authentication can be configured between servers by using the Open Authorization (OAuth) protocol.</span></span> <span data-ttu-id="800ae-127">Par exemple, vous pouvez configurer Lync Server 2013 pour s’authentifier auprès d’un serveur exécutant Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="800ae-127">For example, you can configure Lync Server 2013 to authenticate with a server that is running Exchange Server 2013.</span></span> <span data-ttu-id="800ae-128">À l’aide du protocole OAuth, le serveur Lync et le serveur Exchange peuvent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="800ae-128">Using the OAuth protocol, the Lync server and the Exchange server can trust each other.</span></span> <span data-ttu-id="800ae-129">Cela permet d’intégrer les produits de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="800ae-129">This provides the ability to integrate the products in a seamless manner.</span></span> <span data-ttu-id="800ae-130">Pour plus d’informations, reportez-vous à [gestion des applications d’authentification de serveur à serveur (OAuth) et de partenaire dans Lync server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)</span><span class="sxs-lookup"><span data-stu-id="800ae-130">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)</span></span>

</div>

<div>

## <a name="windows-powershell-based-management-and-web-based-management-interface"></a><span data-ttu-id="800ae-131">Interface de gestion Windows PowerShell et web</span><span class="sxs-lookup"><span data-stu-id="800ae-131">Windows PowerShell-based management and Web-based Management Interface</span></span>

<span data-ttu-id="800ae-132">Lync Server 2013 fournit une interface de gestion puissante, basée sur l’interface de ligne de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="800ae-132">Lync Server 2013 provides a powerful management interface, built on the Windows PowerShell command-line interface.</span></span> <span data-ttu-id="800ae-133">Il inclut des cmdlets de gestion de la sécurité et les fonctionnalités de sécurité de Windows PowerShell sont activées par défaut, de sorte que les utilisateurs ne peuvent pas facilement exécuter des scripts.</span><span class="sxs-lookup"><span data-stu-id="800ae-133">It includes cmdlets for managing security, and Windows PowerShell security features are enabled by default so that users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="800ae-134">Cela signifie que les logiciels par défaut sont configurés pour renforcer la sécurité et réduire les possibilités d’attaque.</span><span class="sxs-lookup"><span data-stu-id="800ae-134">This means that the software defaults are set to automatically help maximize security and reduce the avenues of attack.</span></span> <span data-ttu-id="800ae-135">Pour plus d’informations sur la prise en charge de Windows PowerShell Management dans Lync Server 2013, voir [Lync server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="800ae-135">For details about Windows PowerShell management support in Lync Server 2013, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="role-based-access-control-rbac"></a><span data-ttu-id="800ae-136">Contrôle d’accès basé sur un rôle (RBAC)</span><span class="sxs-lookup"><span data-stu-id="800ae-136">Role-Based Access Control (RBAC)</span></span>

<span data-ttu-id="800ae-137">Microsoft Lync Server 2013 fournit un contrôle d’accès basé sur les rôles (RBAC) pour vous permettre de déléguer des tâches administratives tout en préservant la sécurité des normes.</span><span class="sxs-lookup"><span data-stu-id="800ae-137">Microsoft Lync Server 2013 provides role-based access control (RBAC) to enable you to delegate administrative tasks while maintaining high standards for security.</span></span> <span data-ttu-id="800ae-138">You can use RBAC to follow the principle of "least privilege," in which users are given only the administrative rights that their jobs require.</span><span class="sxs-lookup"><span data-stu-id="800ae-138">You can use RBAC to follow the principle of "least privilege," in which users are given only the administrative rights that their jobs require.</span></span> <span data-ttu-id="800ae-139">Lync Server 2013 introduit la possibilité de créer un nouveau rôle et de modifier un rôle existant.</span><span class="sxs-lookup"><span data-stu-id="800ae-139">Lync Server 2013 introduces the ability to create a new role and also the ability to modify an existing role.</span></span> <span data-ttu-id="800ae-140">Pour plus d’informations, reportez-vous à [planification du contrôle d’accès basé sur les rôles dans Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="800ae-140">For details, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

</div>

</div>

<div>

## <a name="network-address-translation-nat"></a><span data-ttu-id="800ae-141">Traduction d’adresses réseau (NAT)</span><span class="sxs-lookup"><span data-stu-id="800ae-141">Network Address Translation (NAT)</span></span>

<span data-ttu-id="800ae-142">Lync Server 2013 ne prend pas en charge l’utilisation de la traduction d’adresses réseau (NAT) sur l’interface interne du serveur Edge, mais il prend en charge la mise à niveau de l’interface externe du service Edge d’accès, du service Edge de conférence Web et du service Edge A/V d’un routeur ou d’un pare-feu qui effectue une traduction d’adresses réseau (NAT) pour les</span><span class="sxs-lookup"><span data-stu-id="800ae-142">Lync Server 2013 does not support the use of network address translation (NAT) on the internal interface of the Edge Server, but it does support placing the external interface of the Access Edge service, Web Conferencing Edge service, and A/V Edge service behind a router or firewall that performs network address translation (NAT) for both single and scaled consolidated Edge Server topologies.</span></span> <span data-ttu-id="800ae-143">S’il y a plusieurs serveurs Edge utilisant un programme d’équilibrage de la charge matérielle, ils ne peuvent pas utiliser la traduction d’adresses réseau.</span><span class="sxs-lookup"><span data-stu-id="800ae-143">Multiple Edge Servers behind a hardware load balancer cannot use NAT.</span></span> <span data-ttu-id="800ae-144">Si plusieurs serveurs Edge utilisent la traduction d’adresses réseau sur leurs interfaces externes, l’équilibrage de la charge DNS (Domain Name System) est requise.</span><span class="sxs-lookup"><span data-stu-id="800ae-144">If multiple Edge Servers use NAT on their external interfaces, Domain Name System (DNS) load balancing is required.</span></span> <span data-ttu-id="800ae-145">L’utilisation de l’équilibrage de la charge DNS vous permet de réduire le nombre d’adresses IP publiques par serveur Edge dans un pool de serveurs Edge.</span><span class="sxs-lookup"><span data-stu-id="800ae-145">In turn, using DNS load balancing allows you to reduce the number of public IP addresses per Edge Server in an Edge Server pool.</span></span> <span data-ttu-id="800ae-146">Pour plus d’informations, reportez-vous à la[planification de l’accès des utilisateurs externes dans Lync Server 2013](lync-server-2013-planning-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="800ae-146">For details, see[Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="800ae-147">Si vous vous fédérez avec des entreprises qui ont un déploiement de Microsoft Office Communications Server 2007 et que vous devez utiliser l’audio et la vidéo entre votre entreprise et une entreprise fédérée, les ports utilisés seront ceux de l’ancienne version des serveurs Edge déployés.</span><span class="sxs-lookup"><span data-stu-id="800ae-147">If you federate with enterprises that have a Microsoft Office Communications Server 2007 deployment and you need to use audio/video between your enterprise and the federated enterprise, the port requirements will be those for the older version of the Edge Servers that are deployed.</span></span> <span data-ttu-id="800ae-148">Par exemple, les plages de ports requises pour ces versions antérieures doivent être ouvertes pour les deux entreprises tant que le partenaire fédéré a mis à niveau ses serveurs Edge vers Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="800ae-148">For example, the port ranges required for those older versions must be opened for both enterprises until the federated partner upgrades its Edge Servers to Lync Server 2013.</span></span> <span data-ttu-id="800ae-149">Les exigences relatives aux ports peuvent alors être réévaluées et réduites, conformément à la nouvelle configuration.</span><span class="sxs-lookup"><span data-stu-id="800ae-149">At that time, the port requirements can be reviewed and reduced according to the new configuration.</span></span>



</div>

</div>

<div>

## <a name="simplified-certificates-for-edge-servers"></a><span data-ttu-id="800ae-150">Certificats simplifiés pour les serveurs Edge</span><span class="sxs-lookup"><span data-stu-id="800ae-150">Simplified Certificates for Edge Servers</span></span>

<span data-ttu-id="800ae-151">L’Assistant Déploiement peut renseigner automatiquement les noms du sujet et les autres noms du sujet, et minimiser ainsi la possibilité d’inclure des entrées inutiles et éventuellement non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="800ae-151">The Deployment Wizard can automatically populate subject names (SNs) and subject alternative names (SANs), reducing the possibility of including unnecessary and potentially unsecure entries.</span></span>

</div>

<div>

## <a name="trustworthy-computing-security-development-lifecycle-sdl"></a><span data-ttu-id="800ae-152">Cycle de développement d’une sécurité informatique fiable</span><span class="sxs-lookup"><span data-stu-id="800ae-152">Trustworthy Computing Security Development Lifecycle (SDL)</span></span>

<span data-ttu-id="800ae-153">Lync Server 2013 est conçu et développé conformément au cycle de vie de développement de la sécurité Microsoft Trustworthy Computing (SDL), qui est décrit à la section <https://go.microsoft.com/fwlink/?linkid=68761> .</span><span class="sxs-lookup"><span data-stu-id="800ae-153">Lync Server 2013 is designed and developed in compliance with the Microsoft Trustworthy Computing Security Development Lifecycle (SDL), which is described at <https://go.microsoft.com/fwlink/?linkid=68761>.</span></span>

  - <span data-ttu-id="800ae-154">**Fiabilité par conception**   La première étape de la création d’un système de communication unifiée est de concevoir des modèles de menace et de tester chaque fonctionnalité à mesure qu’elle a été conçue.</span><span class="sxs-lookup"><span data-stu-id="800ae-154">**Trustworthy by Design**   The first step in creating a more secure unified communications system was to design threat models and test each feature as it was designed.</span></span> <span data-ttu-id="800ae-155">De plus, Microsoft effectue des tests sur des comportements anormaux afin de détecter les failles de sécurité résultant d’un comportement inattendu du produit.</span><span class="sxs-lookup"><span data-stu-id="800ae-155">In addition, Microsoft performs testing outside of the designed behavior in order to find security vulnerabilities resulting from unexpected product behavior.</span></span> <span data-ttu-id="800ae-156">Plusieurs améliorations liées à la sécurité ont été intégrées dans le processus et les pratiques de codage.</span><span class="sxs-lookup"><span data-stu-id="800ae-156">Multiple security-related improvements were built into the coding process and practices.</span></span> <span data-ttu-id="800ae-157">Au moment de la création, des outils détectent les dépassements de mémoire tampon et d’autres risques de sécurité potentiels avant l’archivage du code dans le produit final.</span><span class="sxs-lookup"><span data-stu-id="800ae-157">Build-time tools detect buffer overruns and other potential security threats before the code is checked in to the final product.</span></span> <span data-ttu-id="800ae-158">Bien sûr, il est impossible de prévoir toutes les menaces de sécurités inconnues lors de la conception.</span><span class="sxs-lookup"><span data-stu-id="800ae-158">Of course, it is impossible to design against all unknown security threats.</span></span> <span data-ttu-id="800ae-159">Aucun système ne peut garantir une sécurité totale.</span><span class="sxs-lookup"><span data-stu-id="800ae-159">No system can guarantee complete security.</span></span> <span data-ttu-id="800ae-160">Toutefois, étant donné que le développement de produits a adopté des principes de conception sécurisés depuis le début, Lync Server 2013 inclut les technologies de sécurité standard de l’industrie comme partie fondamentales de son architecture.</span><span class="sxs-lookup"><span data-stu-id="800ae-160">However, because product development embraced secure design principles from the start, Lync Server 2013 incorporates industry standard security technologies as a fundamental part of its architecture.</span></span>

  - <span data-ttu-id="800ae-161">**Digne de confiance par défaut**   Par défaut, les communications réseau dans Lync Server 2013 sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="800ae-161">**Trustworthy by Default**   By default, network communications in Lync Server 2013 are encrypted.</span></span> <span data-ttu-id="800ae-162">Dans la mesure où tous les serveurs utilisent les certificats et l’authentification Kerberos, TLS, Secure Real-Time Transport Protocol (SRTP) et d’autres techniques de chiffrement standard, dont le chiffrement AES (Advanced Encryption Standard) 128, toutes les données du serveur Lync sont protégées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="800ae-162">Because all servers use certificates and Kerberos authentication, TLS, Secure Real-Time Transport Protocol (SRTP), and other industry-standard encryption techniques, including 128-bit Advanced Encryption Standard (AES) encryption, virtually all Lync Server data is protected on the network.</span></span> <span data-ttu-id="800ae-163">De plus, le contrôle d’accès basé sur les rôles permet de déployer des serveurs exécutant Lync Server 2013 de sorte que chaque rôle de serveur exécute uniquement les services et que seules les autorisations associées à ces services soient appropriées pour le rôle serveur.</span><span class="sxs-lookup"><span data-stu-id="800ae-163">In addition, role-based access control makes it possible to deploy servers running Lync Server 2013 so that each server role runs only the services, and has only the permissions related to those services, that are appropriate for the server role.</span></span>

  - <span data-ttu-id="800ae-164">**Fiabilité du déploiement**   Toute la documentation Lync Server 2013 inclut des pratiques recommandées et des recommandations pour vous aider à déterminer et configurer les niveaux de sécurité optimaux pour votre déploiement et à évaluer les risques en matière de sécurité liés à l’activation des options non par défaut.</span><span class="sxs-lookup"><span data-stu-id="800ae-164">**Trustworthy by Deployment**   All Lync Server 2013 documentation includes best practices and recommendations to help you determine and configure the optimal security levels for your deployment and assess the security risks of activating non-default options.</span></span>

<span data-ttu-id="800ae-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="800ae-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

