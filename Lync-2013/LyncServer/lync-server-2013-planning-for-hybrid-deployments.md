---
title: 'Lync Server 2013 : Planification des déploiements hybrides'
description: 'Lync Server 2013 : Planification des déploiements hybrides.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424547"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="48777-103">Planification des déploiements hybrides Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48777-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48777-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48777-104">

<span> </span></span></span>

<span data-ttu-id="48777-105">_**Rubrique dernière modification :** 2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="48777-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="48777-106">Vous devez tenir compte des exigences suivantes pour les utilisateurs et votre infrastructure réseau lors de la planification d’un déploiement hybride.</span><span class="sxs-lookup"><span data-stu-id="48777-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="48777-107">Conditions requises pour l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="48777-107">Infrastructure Requirements</span></span>

<span data-ttu-id="48777-108">Pour implémenter et déployer un déploiement hybride, vous devez configurer les configurations suivantes dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="48777-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="48777-109">Organisation Microsoft 365 ou Office 365 avec Skype Entreprise Online activé.</span><span class="sxs-lookup"><span data-stu-id="48777-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="48777-110">Notez que vous ne pouvez utiliser qu’un seul client pour une configuration hybride avec votre déploiement local.</span><span class="sxs-lookup"><span data-stu-id="48777-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="48777-111">Un seul déploiement local (infrastructure) de Skype Entreprise Server ou de Lync Server déployé dans une topologie prise en charge.</span><span class="sxs-lookup"><span data-stu-id="48777-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="48777-112">Consultez la topologie requise.</span><span class="sxs-lookup"><span data-stu-id="48777-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="48777-113">Pour plus d’informations sur la configuration de votre déploiement Lync Server 2013 ou Lync Server 2010 pour un déploiement hybride, voir Configuration des [déploiements hybrides de Lync Server 2013.](lync-server-2013-configuring-hybrid-deployments.md)</span><span class="sxs-lookup"><span data-stu-id="48777-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="48777-114">Outils d’administration Skype Entreprise Server 2015.</span><span class="sxs-lookup"><span data-stu-id="48777-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="48777-115">Si vous utilisez Lync Server 2013 ou Lync Server 2010, vous pouvez utiliser les outils d’administration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48777-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="48777-116">Pour prendre en charge l’authentification unique avec Microsoft 365 ou Office 365, afin que les utilisateurs peuvent utiliser les mêmes informations d’identification pour se connecter à Office et pour se connecter en local, vous pouvez utiliser les fonctionnalités de synchronisation des mots de passe d’Azure Active Directory (AAD) Connect.</span><span class="sxs-lookup"><span data-stu-id="48777-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="48777-117">Vous pouvez également utiliser les services AD FS (Active Directory Federation Services) pour l' sign-on unique avec Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="48777-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="48777-118">Pour plus d’informations, voir Intégration de vos [identités locales avec Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)</span><span class="sxs-lookup"><span data-stu-id="48777-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="48777-119">Une solution de synchronisation d’annuaires unique pour assurer la synchronisation de vos objets Active Directory locaux et en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="48777-120">Pour plus d’informations sur la synchronisation d’annuaires, voir [Outils d’intégration d’annuaire.](https://go.microsoft.com/fwlink/p/?linkid=530320)</span><span class="sxs-lookup"><span data-stu-id="48777-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="48777-121">Lync Client Support</span><span class="sxs-lookup"><span data-stu-id="48777-121">Lync Client Support</span></span>

<span data-ttu-id="48777-122">Il existe des différences entre les fonctionnalités pris en charge dans les clients Lync, ainsi que dans les fonctionnalités disponibles dans les environnements locaux et en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="48777-123">Avant de choisir l’emplacement où vous souhaitez home les utilisateurs dans votre organisation, vous pouvez consulter le support client pour les différentes configurations de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="48777-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="48777-124">Les clients suivants sont pris en charge avec Skype Entreprise Online dans un déploiement hybride Lync :</span><span class="sxs-lookup"><span data-stu-id="48777-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="48777-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="48777-125">Lync 2010</span></span>

  - <span data-ttu-id="48777-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="48777-126">Lync 2013</span></span>

  - <span data-ttu-id="48777-127">application Lync du Windows Store</span><span class="sxs-lookup"><span data-stu-id="48777-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="48777-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="48777-128">Lync Web App</span></span>

  - <span data-ttu-id="48777-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="48777-129">Lync Mobile</span></span>

  - <span data-ttu-id="48777-130">Lync pour Mac 2011</span><span class="sxs-lookup"><span data-stu-id="48777-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="48777-131">Lync Room System</span><span class="sxs-lookup"><span data-stu-id="48777-131">Lync Room System</span></span>

  - <span data-ttu-id="48777-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="48777-132">Lync Basic 2013</span></span>

<span data-ttu-id="48777-133">Pour plus d’informations sur le support client, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="48777-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="48777-134">Clients pour Lync Online</span><span class="sxs-lookup"><span data-stu-id="48777-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="48777-135">Tableau de comparaison des clients pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48777-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="48777-136">Tableau de comparaison des clients mobiles pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48777-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="48777-137">Conditions requises pour la topologie</span><span class="sxs-lookup"><span data-stu-id="48777-137">Topology Requirements</span></span>

<span data-ttu-id="48777-138">Pour configurer votre déploiement pour un déploiement hybride avec Skype Entreprise Online, l’une des topologies suivantes doit être prise en charge :</span><span class="sxs-lookup"><span data-stu-id="48777-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="48777-139">Déploiement de Skype Entreprise Server 2015 avec tous les serveurs exécutant Skype Entreprise Server 2015.</span><span class="sxs-lookup"><span data-stu-id="48777-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="48777-140">Déploiement de Lync Server 2013 avec tous les serveurs exécutant Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48777-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="48777-141">Un déploiement Lync Server 2010 avec tous les serveurs exécutant Lync Server 2010 avec les dernières mises à jour cumulatives.</span><span class="sxs-lookup"><span data-stu-id="48777-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="48777-142">Le serveur Edge de fédération et le serveur du saut suivant à partir du serveur Edge de fédération doivent exécutent Lync Server 2010 avec les dernières mises à jour cumulatives.</span><span class="sxs-lookup"><span data-stu-id="48777-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="48777-143">Les outils d’administration de Skype Entreprise Server 2015 ou Lync Server 2013 doivent être installés sur au moins un serveur ou une station de travail de gestion.</span><span class="sxs-lookup"><span data-stu-id="48777-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="48777-144">Déploiement mixte de Lync Server 2013 et de Skype Entreprise Server 2015 avec les rôles de serveur suivants sur au moins un site exécutant Skype Entreprise Server 2015 :</span><span class="sxs-lookup"><span data-stu-id="48777-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="48777-145">Au moins un pool d'entreprise ou serveur Standard Edition </span><span class="sxs-lookup"><span data-stu-id="48777-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="48777-146">Pool directeur associé à la fédération SIP, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="48777-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="48777-147">Pool Edge associé à la fédération SIP</span><span class="sxs-lookup"><span data-stu-id="48777-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="48777-148">Déploiement mixte de Lync Server 2010 et de Skype Entreprise Server 2015 avec les rôles de serveurs suivants sur au moins un site exécutant Skype Entreprise Server 2015 :</span><span class="sxs-lookup"><span data-stu-id="48777-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="48777-149">Au moins un pool d'entreprise ou serveur Standard Edition </span><span class="sxs-lookup"><span data-stu-id="48777-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="48777-150">Pool directeur associé à la fédération SIP, le cas échéant</span><span class="sxs-lookup"><span data-stu-id="48777-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="48777-151">Pool Edge associé à la fédération SIP pour le site</span><span class="sxs-lookup"><span data-stu-id="48777-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="48777-152">Déploiement de Lync Server 2010 et Lync Server 2013 mixte avec les rôles de serveur suivants sur au moins un site exécutant Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="48777-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="48777-153">Au moins un pool d'entreprise ou serveur Standard Edition dans le site</span><span class="sxs-lookup"><span data-stu-id="48777-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="48777-154">Pool directeur associé à la fédération SIP, si elle existe dans le site</span><span class="sxs-lookup"><span data-stu-id="48777-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="48777-155">Pool Edge associé à la fédération SIP pour le site</span><span class="sxs-lookup"><span data-stu-id="48777-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="48777-156">La gestion des utilisateurs, y compris les déplacements entre les utilisateurs locaux et UNRESOLVED_TOKEN_VAL (skypeforbusiness) Online, doit être effectuée à l’aide de la dernière version installée des outils d’administration.</span><span class="sxs-lookup"><span data-stu-id="48777-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="48777-157">Les outils d’administration doivent être installés sur un serveur distinct connecté au déploiement local existant et à Internet.</span><span class="sxs-lookup"><span data-stu-id="48777-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="48777-158">L’let <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> pour déplacer les utilisateurs de votre déploiement local vers UNRESOLVED_TOKEN_VAL(skype16_online) doit être exécuté à partir des outils d’administration connectés à votre déploiement local.</span><span class="sxs-lookup"><span data-stu-id="48777-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="48777-159">Pour plus d’informations sur les topologies pris en charge, voir Topologies pris en charge dans [Lync Server 2013](lync-server-2013-supported-topologies.md)et topologies de référence [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)pour les déploiements hybrides d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="48777-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="48777-160">Pour obtenir des informations de dépannage sur les déploiements hybrides et la connexion de PowerShell à Lync Online, voir [Lync Online : Lync PowerShell](https://go.microsoft.com/fwlink/p/?linkid=306718)et résolution des problèmes hybrides.</span><span class="sxs-lookup"><span data-stu-id="48777-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="48777-161">Conditions requises pour les listes de fédération autorisées/bloquées</span><span class="sxs-lookup"><span data-stu-id="48777-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="48777-p108">La liste des domaines autorisés comprend les domaines pour lesquels un nom de domaine complet Edge partenaire est configuré (parfois appelé *serveur partenaire autorisé* ou *partenaire de fédération direct*). Vous devez connaitre la différence entre la fédération ouverte et la fédération fermée, appelée *découverte de partenaire* et *liste de domaines partenaires autorisés*, dans les déploiements locaux.</span><span class="sxs-lookup"><span data-stu-id="48777-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="48777-165">La configuration ci-dessous est requise pour configurer un déploiement hybride :</span><span class="sxs-lookup"><span data-stu-id="48777-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="48777-166">La correspondance de domaine doit être identique pour votre déploiement local et votre organisation Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="48777-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="48777-167">Si la découverte de partenaire est activée sur le déploiement local, la fédération ouverte doit être configurée pour votre client en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="48777-168">Si la découverte de partenaire n'est pas activée, alors la fédération fermée doit être configurée pour votre client en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="48777-169">La liste des domaines bloqués dans le déploiement local doit correspondre exactement à la liste des domaines bloqués pour votre client en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="48777-170">La liste des domaines autorisés dans le déploiement local doit correspondre exactement à la liste des domaines autorisés pour votre client en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="48777-171">La fédération doit être activée pour les communications externes pour le client en ligne, qui est configuré à l’aide du Panneau de configuration de Lync Online.</span><span class="sxs-lookup"><span data-stu-id="48777-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="48777-172">Paramètres DNS</span><span class="sxs-lookup"><span data-stu-id="48777-172">DNS Settings</span></span>

<span data-ttu-id="48777-173">Lors de la création d’enregistrements DNS pour les déploiements hybrides, tous les enregistrements DNS externes de Lync doivent pointer vers l’infrastructure locale.</span><span class="sxs-lookup"><span data-stu-id="48777-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="48777-174">Pour plus d’informations sur les enregistrements DNS requis, reportez-vous aux conditions [DNS requises pour Lync Server 2013.](lync-server-2013-domain-name-system-dns-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="48777-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="48777-175">En outre, vous devez vous assurer que la résolution DNS décrite dans le tableau ci-dessous fonctionne dans votre déploiement local :</span><span class="sxs-lookup"><span data-stu-id="48777-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48777-176">Enregistrement DNS</span><span class="sxs-lookup"><span data-stu-id="48777-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="48777-177">Résolvable par</span><span class="sxs-lookup"><span data-stu-id="48777-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="48777-178">Enregistrement DNS requis</span><span class="sxs-lookup"><span data-stu-id="48777-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48777-179">Enregistrement SRV DNS pour _sipfederationtls._tcp. &lt; sipdomain.com pour tous les domaines SIP pris en charge résolvant vers des adresses IP externes &gt; Access Edge</span><span class="sxs-lookup"><span data-stu-id="48777-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="48777-180">Serveur(s) Edge</span><span class="sxs-lookup"><span data-stu-id="48777-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="48777-p111">Permettre la communication fédérée dans une configuration hybride. Le serveur Edge doit savoir où acheminer le trafic fédéré pour le domaine SIP qui est à la fois en local et en ligne.</span><span class="sxs-lookup"><span data-stu-id="48777-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48777-183">Enregistrement(s) DNS A pour le FQDN du service de conférence web Edge, par exemple webcon.contoso.com se résolvant en adresse(s) IP externe(s) Edge de conférence web</span><span class="sxs-lookup"><span data-stu-id="48777-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="48777-184">Ordinateurs des utilisateurs connectés au réseau d'entreprise interne</span><span class="sxs-lookup"><span data-stu-id="48777-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="48777-p112">Permettre aux utilisateurs de présenter ou d'afficher le contenu de réunions hébergées localement. Ce contenu peut inclure des fichiers PowerPoint, des tableaux blancs, des sondages et des notes partagées. </span><span class="sxs-lookup"><span data-stu-id="48777-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48777-187">En fonction de la configuration DNS de votre organisation, vous devrez peut-être ajouter ces enregistrements dans la zone DNS hébergée en interne pour le(s) domaine(s) SIP correspondant(s) afin de fournir à ces enregistrements une résolution DNS interne.</span><span class="sxs-lookup"><span data-stu-id="48777-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="48777-188">Éléments à prendre en compte pour le pare-feu</span><span class="sxs-lookup"><span data-stu-id="48777-188">Firewall Considerations</span></span>

<span data-ttu-id="48777-p113">Les ordinateurs du réseau doivent être en mesure d'effectuer des recherches DNS Internet. Si ces ordinateurs peuvent accéder à des sites Internet standard, votre réseau est correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="48777-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="48777-191">Selon l’emplacement de votre centre de données Microsoft Online Services, vous devez également configurer vos appareils de pare-feu réseau pour accepter les connexions en fonction de noms de domaine génériques (par exemple, tout le trafic en provenance de \* .outlook.com).</span><span class="sxs-lookup"><span data-stu-id="48777-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="48777-192">Si les pare-feu de votre organisation ne prennent pas en charge les configurations de nom génériques, vous devrez déterminer manuellement les plages d'adresses IP que vous voulez autoriser et les ports.</span><span class="sxs-lookup"><span data-stu-id="48777-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="48777-193">Consultez la rubrique d’aide sur les URL et [plages d’adresses IP Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)</span><span class="sxs-lookup"><span data-stu-id="48777-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="48777-194">Exigences en matière de port et de protocole</span><span class="sxs-lookup"><span data-stu-id="48777-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="48777-195">Outre la configuration requise pour les ports pour les communications internes à Lync Server 2013, vous devez également configurer les ports suivants.</span><span class="sxs-lookup"><span data-stu-id="48777-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48777-196">Protocole /Port</span><span class="sxs-lookup"><span data-stu-id="48777-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="48777-197">Applications</span><span class="sxs-lookup"><span data-stu-id="48777-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48777-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="48777-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="48777-199">Ouvrir entrant</span><span class="sxs-lookup"><span data-stu-id="48777-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="48777-200">Services AD FS (rôle serveur de fédération)</span><span class="sxs-lookup"><span data-stu-id="48777-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="48777-201">Pour plus d’informations, voir <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Comprendre les services de rôle d’AD FS.</a></span><span class="sxs-lookup"><span data-stu-id="48777-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="48777-202">Services AD FS (rôle serveur proxy)</span><span class="sxs-lookup"><span data-stu-id="48777-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="48777-203">Microsoft Online Services’entreprise</span><span class="sxs-lookup"><span data-stu-id="48777-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="48777-204">Mon portail d’entreprise</span><span class="sxs-lookup"><span data-stu-id="48777-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="48777-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="48777-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="48777-206">Client Lync (communication avec Lync Online à partir d’un serveur Lync local)</span><span class="sxs-lookup"><span data-stu-id="48777-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48777-207">TCP 80 et 443</span><span class="sxs-lookup"><span data-stu-id="48777-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="48777-208">Ouvrir entrant</span><span class="sxs-lookup"><span data-stu-id="48777-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="48777-209">Microsoft Online Services - Outil de synchronisation d'annuaires</span><span class="sxs-lookup"><span data-stu-id="48777-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48777-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="48777-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="48777-211">Ouvrir entrant/sortant sur le serveur Edge</span><span class="sxs-lookup"><span data-stu-id="48777-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48777-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="48777-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="48777-213">Ouvrir entrant/sortant pour les sessions de partage de données</span><span class="sxs-lookup"><span data-stu-id="48777-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48777-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="48777-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="48777-215">Ouvrir entrant/sortant pour les sessions de partage audio, vidéo et d’application</span><span class="sxs-lookup"><span data-stu-id="48777-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48777-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="48777-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="48777-217">Ouvrir entrant/sortant pour les sessions audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="48777-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48777-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="48777-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="48777-219">Ouvrir sortant pour les sessions audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="48777-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="48777-220">Comptes et données d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="48777-220">User Accounts and Data</span></span>

<span data-ttu-id="48777-221">Dans un déploiement hybride Lync Server 2013, tout utilisateur que vous souhaitez home dans Lync Online doit d’abord être créé dans le déploiement local afin que le compte d’utilisateur soit créé dans les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="48777-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="48777-222">Vous pouvez ensuite déplacer l’utilisateur vers Skype Entreprise Online afin de déplacer sa liste de contacts.</span><span class="sxs-lookup"><span data-stu-id="48777-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="48777-223">Lorsque vous synchronisez les comptes d’utilisateurs entre vos déploiements Lync local et Lync Online avec AD FS et Dirsync, vous devez synchroniser les comptes AD de tous les utilisateurs Lync de votre organisation entre vos déploiements Lync locaux et en ligne, même si les utilisateurs ne sont pas déplacés vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="48777-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="48777-224">Si vous ne synchronisez pas tous les utilisateurs, la communication entre les utilisateurs locaux et en ligne dans votre organisation risque de ne pas fonctionner comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="48777-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="48777-225">Si l’utilisateur est créé à l’aide du portail en ligne du Centre d’administration Microsoft 365, le compte d’utilisateur n’est pas synchronisé avec Active Directory local et l’utilisateur n’existera pas dans l’Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="48777-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="48777-226">Si vous avez déjà créé des utilisateurs dans Lync Online et que vous souhaitez configurer un hybride avec un serveur Lync local, consultez Déplacer des utilisateurs de Lync Online vers Lync local dans <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="48777-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="48777-227">Lors de la planification d'un déploiement hybride, prenez en compte les aspects suivants liés aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="48777-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="48777-228">**Contacts de l’utilisateur**   La limite de contacts pour les utilisateurs de Lync Online est de 250.</span><span class="sxs-lookup"><span data-stu-id="48777-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="48777-229">Au-delà de ce chiffre, les contacts seront supprimés de la liste des contacts de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48777-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="48777-230">**Messagerie instantanée et présence**   Les listes de contacts, groupes et listes de contrôle d'accès des utilisateurs sont migrés avec le compte de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48777-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="48777-231">**Données de conférence, contenu de réunion et réunions programmées**   Ce contenu n’est pas migré avec le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48777-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="48777-232">Les utilisateurs doivent replanifier les réunions une fois leur compte migré sur Lync Online.</span><span class="sxs-lookup"><span data-stu-id="48777-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="48777-233">Fonctionnalités et stratégies utilisateur</span><span class="sxs-lookup"><span data-stu-id="48777-233">User Policies and Features</span></span>

  - <span data-ttu-id="48777-234">Dans un environnement hybride Lync Server 2013, les utilisateurs peuvent utiliser la messagerie instantanée, la voix et les réunions en local ou en ligne, mais pas les deux simultanément.</span><span class="sxs-lookup"><span data-stu-id="48777-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="48777-235">**Client Lync**    Certains utilisateurs peuvent avoir besoin d’une nouvelle version du client lorsqu’ils sont déplacés vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="48777-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="48777-236">Pour Office Communications Server 2007 R2, les utilisateurs doivent être déplacés vers un pool Lync Server 2013 avant la migration vers Lync Online.</span><span class="sxs-lookup"><span data-stu-id="48777-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="48777-237">Pour plus d’informations sur le support client, voir [Clients pour Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) et les clients Lync pris en charge et les [configurations de ports réseau.](https://go.microsoft.com/fwlink/p/?linkid=281901)</span><span class="sxs-lookup"><span data-stu-id="48777-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="48777-238">**Configuration et stratégies sur site (non-utilisateur)**   Les stratégies en ligne et sur site nécessitent une configuration distincte.</span><span class="sxs-lookup"><span data-stu-id="48777-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="48777-239">Vous ne pouvez pas définir des stratégies globales qui s'appliquent au deux.</span><span class="sxs-lookup"><span data-stu-id="48777-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="48777-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48777-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
