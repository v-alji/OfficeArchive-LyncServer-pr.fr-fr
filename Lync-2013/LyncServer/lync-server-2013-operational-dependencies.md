---
title: 'Lync Server 2013 : dépendances opérationnelles'
description: 'Lync Server 2013 : dépendances opérationnelles.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445294"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="1c913-103">Dépendances opérationnelles dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c913-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c913-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c913-104">

<span> </span></span></span>

<span data-ttu-id="1c913-105">_**Dernière modification de la rubrique :** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="1c913-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="1c913-106">L’architecture de référence décrite dans ce document permet de vérifier que vous disposez d’un déploiement 2013 Server Lync qui n’est pas uniquement destiné aux besoins de l’organisation, mais qu’il est structuré conformément aux meilleures pratiques Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1c913-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="1c913-107">Soyez qu’il est possible que l’implémentation de Lync Server 2013 soit un service dynamique et que tous les autres services de l’entreprise requièrent une analyse et une gestion proactive pour maintenir un niveau élevé de disponibilité et de qualité de service pour l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1c913-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="1c913-108">Dans la mesure où Lync Server 2013 devient profondément en grain dans l’entreprise, il est important que le service soit géré par une gestion précise et tangible du niveau de service.</span><span class="sxs-lookup"><span data-stu-id="1c913-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="1c913-109">L’architecture système de Lync peut devenir complexe et très intégrée et permettre de maintenir une gestion de niveau de service effective et de définir les SLA pour Lync Server 2013 il est essentiel de comprendre les dépendances du système sur d’autres plateformes et serveurs.</span><span class="sxs-lookup"><span data-stu-id="1c913-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="1c913-110">Il est également important de noter quels services d’entreprise, tels que les applications vocales et les applications intégrées de Cu, dépendent de Lync.</span><span class="sxs-lookup"><span data-stu-id="1c913-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="1c913-111">Lync Server 2013 doit être établi en indiquant toutes les dépendances.</span><span class="sxs-lookup"><span data-stu-id="1c913-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="1c913-112">Le plan de service vous permet d’élaborer un SLA entre Lync et son service dépendant et de fournir un emplacement de départ pour la négociation SLA.</span><span class="sxs-lookup"><span data-stu-id="1c913-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="1c913-113">Le tableau suivant répertorie les services de dépendance typiques pour une infrastructure Lync.</span><span class="sxs-lookup"><span data-stu-id="1c913-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="1c913-114">Chacune de ces technologies doit avoir son propre contrôle proactif.</span><span class="sxs-lookup"><span data-stu-id="1c913-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="1c913-115">Services de dépendance typiques</span><span class="sxs-lookup"><span data-stu-id="1c913-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c913-116">Service de dépendance</span><span class="sxs-lookup"><span data-stu-id="1c913-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c913-117">Systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1c913-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-118">Matériel du serveur</span><span class="sxs-lookup"><span data-stu-id="1c913-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="1c913-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-120">Infrastructure à clé publique</span><span class="sxs-lookup"><span data-stu-id="1c913-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-121">Service d’attribution de noms de domaine</span><span class="sxs-lookup"><span data-stu-id="1c913-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-122">Services de base de données</span><span class="sxs-lookup"><span data-stu-id="1c913-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-123">Storage Services</span><span class="sxs-lookup"><span data-stu-id="1c913-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-124">Gestion du système – surveillance et distribution</span><span class="sxs-lookup"><span data-stu-id="1c913-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-125">Services de sécurité-antivirus</span><span class="sxs-lookup"><span data-stu-id="1c913-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-126">Infrastructure réseau-Internet</span><span class="sxs-lookup"><span data-stu-id="1c913-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-127">Infrastructure réseau-interne (LAN/WAN)</span><span class="sxs-lookup"><span data-stu-id="1c913-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-128">Infrastructure de téléphonie – PBX IP et passerelles</span><span class="sxs-lookup"><span data-stu-id="1c913-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-129">Services Cloud</span><span class="sxs-lookup"><span data-stu-id="1c913-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c913-130">Il est supposé que l’organisation s’est imposée par le biais des fonctions de gestion de niveau de service de base, telles que la modification, l’incident et la gestion des versions, conformément au programme MOF.</span><span class="sxs-lookup"><span data-stu-id="1c913-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="1c913-131">La solution Lync doit être adoptée par ces fonctions et être soumise aux mêmes processus de gestion opérationnels.</span><span class="sxs-lookup"><span data-stu-id="1c913-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="1c913-132">Outre les informations fournies ci-dessus, nous avons à présent une connaissance plus approfondie des éléments qui peuvent avoir un impact sur le service Lync au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1c913-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="1c913-133">Pour garantir la disponibilité et la qualité du service Lync Server 2013, les outils d’analyse suivants doivent accompagner le déploiement de l’architecture de référence :</span><span class="sxs-lookup"><span data-stu-id="1c913-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="1c913-134">Outils d’analyse</span><span class="sxs-lookup"><span data-stu-id="1c913-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c913-135">Composant</span><span class="sxs-lookup"><span data-stu-id="1c913-135">Component</span></span></th>
<th><span data-ttu-id="1c913-136">Description</span><span class="sxs-lookup"><span data-stu-id="1c913-136">Description</span></span></th>
<th><span data-ttu-id="1c913-137">Site applicable</span><span class="sxs-lookup"><span data-stu-id="1c913-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c913-138">Serveur de surveillance Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c913-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="1c913-139">Déploiement d’au moins un rôle de serveur Lync Server 2013 de surveillance par site central et de configuration du Pack de rapport qualité de l’interface (QoE).</span><span class="sxs-lookup"><span data-stu-id="1c913-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="1c913-140">Pour plus d’informations, reportez-vous à la documentation sur le déploiement de Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="1c913-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="1c913-141"><a href="lync-server-2013-deploying-monitoring.md">Déploiement de la surveillance dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="1c913-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="1c913-142">Sites centraux</span><span class="sxs-lookup"><span data-stu-id="1c913-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-143">Attachez chaque liste à l’instance la plus proche du rôle serveur de surveillance.</span><span class="sxs-lookup"><span data-stu-id="1c913-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="1c913-144">Sites centraux</span><span class="sxs-lookup"><span data-stu-id="1c913-144">Central sites</span></span></p>
<p><span data-ttu-id="1c913-145">Sites de succursales</span><span class="sxs-lookup"><span data-stu-id="1c913-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="1c913-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="1c913-147">L’importation de System Center Operations Manager 2012 avec le pack d’administration Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1c913-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="1c913-148">Le pack d’administration implémente le journal des événements traditionnel et l’instrumentation basée sur le compteur de performance, ainsi que l’activation de l’instrumentation nouvellement disponible dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1c913-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="1c913-149">Sites centraux</span><span class="sxs-lookup"><span data-stu-id="1c913-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-150">Assurez-vous que la recherche centralisée de rôles et de composants à surveiller est effectuée automatiquement en fonction d’un script de découverte centralisé qui lit le document de topologie publié dans la base de données de gestion centrale.</span><span class="sxs-lookup"><span data-stu-id="1c913-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="1c913-151">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-151">Central Site</span></span></p>
<p><span data-ttu-id="1c913-152">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-152">Branch Site</span></span></p>
<p><span data-ttu-id="1c913-153">Site Edge</span><span class="sxs-lookup"><span data-stu-id="1c913-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="1c913-154">Déployez les agents 2007 de System Center Operations Manager sur tous les serveurs déployés exécutant Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c913-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="1c913-155">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-155">Central Site</span></span></p>
<p><span data-ttu-id="1c913-156">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-156">Branch Site</span></span></p>
<p><span data-ttu-id="1c913-157">Site Edge</span><span class="sxs-lookup"><span data-stu-id="1c913-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-158">Vérifiez que les alertes classées sont configurées pour la notification :</span><span class="sxs-lookup"><span data-stu-id="1c913-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="1c913-159">Alertes de priorité élevée</span><span class="sxs-lookup"><span data-stu-id="1c913-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="1c913-160">Alertes de priorité moyenne</span><span class="sxs-lookup"><span data-stu-id="1c913-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="1c913-161">Autres alertes.</span><span class="sxs-lookup"><span data-stu-id="1c913-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="1c913-162">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-162">Central Site</span></span></p>
<p><span data-ttu-id="1c913-163">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-163">Branch Site</span></span></p>
<p><span data-ttu-id="1c913-164">Site Edge</span><span class="sxs-lookup"><span data-stu-id="1c913-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="1c913-165">Configurer le contrôle de port pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="1c913-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="1c913-166">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-166">Central Site</span></span></p>
<p><span data-ttu-id="1c913-167">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-167">Branch Site</span></span></p>
<p><span data-ttu-id="1c913-168">Site Edge</span><span class="sxs-lookup"><span data-stu-id="1c913-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-169">Configurer le contrôle d’URL pour votre déploiement</span><span class="sxs-lookup"><span data-stu-id="1c913-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="1c913-170">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-171">Intégration de Lync et System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="1c913-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="1c913-172">Déploiement de la fiabilité des appels et de la qualité multimédia MonitoringCall de la fiabilité et de la qualité multimédia utilisez l’ordinateur de surveillance serveur comme nœud d’observation pour contrôler la fiabilité des appels et la qualité multimédia de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1c913-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="1c913-173">Ces deux fonctionnalités interrogeront les bases de données du serveur de surveillance pour analyse.</span><span class="sxs-lookup"><span data-stu-id="1c913-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="1c913-174">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-174">Central Site</span></span></p>
<p><span data-ttu-id="1c913-175">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-176">Vérifiez que les seuils d’avertissement de qualité multimédia sont correctement configurés.</span><span class="sxs-lookup"><span data-stu-id="1c913-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="1c913-177">Le tableau suivant indique le nombre maximal d’avis de moyenne réseau par codec.</span><span class="sxs-lookup"><span data-stu-id="1c913-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="1c913-178">En production, ces scores doivent être surveillés pour une période donnée et le seuil acceptable doit être établi en fonction des scores de NMOS spécifiques de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1c913-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="1c913-179">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-179">Central Site</span></span></p>
<p><span data-ttu-id="1c913-180">Site de succursale</span><span class="sxs-lookup"><span data-stu-id="1c913-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-181">Observateur de transactions synthétiques de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c913-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="1c913-182">Déploiement d’un serveur Lync dédié en tant qu’observateur de transactions synthétiques.</span><span class="sxs-lookup"><span data-stu-id="1c913-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="1c913-183">Les transactions synthétiques sont des cmdlets Windows PowerShell Lync Server 2013 qui sont automatiquement déclenchées par le pack d’administration sur un intervalle prédéfini.</span><span class="sxs-lookup"><span data-stu-id="1c913-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="1c913-184">Celles-ci sont exécutées sur un nœud d’observateur de transactions synthétique qui est un serveur désigné par un administrateur responsable de la découverte et de l’exécution de STs pour chaque pool.</span><span class="sxs-lookup"><span data-stu-id="1c913-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="1c913-185">Nous vous déconseillons d’utiliser un serveur Microsoft Lync Server 2013 existant en tant que nœud de l’observateur de transactions synthétiques.</span><span class="sxs-lookup"><span data-stu-id="1c913-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="1c913-186">En raison de la configuration requise pour l’utilisation du service STs.</span><span class="sxs-lookup"><span data-stu-id="1c913-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="1c913-187">Utilisez un nouvel ordinateur serveur (ou un serveur virtuel) pour le nœud de l’observateur de transactions synthétique.</span><span class="sxs-lookup"><span data-stu-id="1c913-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="1c913-188">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="1c913-189">Déploiement du nœud d’observation de transactions synthétiques.</span><span class="sxs-lookup"><span data-stu-id="1c913-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="1c913-190">Reportez-vous au document de MonitoringCS_withSCOM.docx à partir de la documentation UCTAP Connect.</span><span class="sxs-lookup"><span data-stu-id="1c913-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="1c913-191">Site central</span><span class="sxs-lookup"><span data-stu-id="1c913-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="1c913-192">Scores de réseau maximal par codec</span><span class="sxs-lookup"><span data-stu-id="1c913-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c913-193">Scénario</span><span class="sxs-lookup"><span data-stu-id="1c913-193">Scenario</span></span></th>
<th><span data-ttu-id="1c913-194">Codec</span><span class="sxs-lookup"><span data-stu-id="1c913-194">Codec</span></span></th>
<th><span data-ttu-id="1c913-195">NMOS Max</span><span class="sxs-lookup"><span data-stu-id="1c913-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c913-196">UC UC-appel d’UC</span><span class="sxs-lookup"><span data-stu-id="1c913-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="1c913-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="1c913-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="1c913-198">4,10</span><span class="sxs-lookup"><span data-stu-id="1c913-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-199">UC UC-appel d’UC</span><span class="sxs-lookup"><span data-stu-id="1c913-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="1c913-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="1c913-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="1c913-201">2,95</span><span class="sxs-lookup"><span data-stu-id="1c913-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-202">Téléconférence</span><span class="sxs-lookup"><span data-stu-id="1c913-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="1c913-203">Siren</span><span class="sxs-lookup"><span data-stu-id="1c913-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="1c913-204">3,72</span><span class="sxs-lookup"><span data-stu-id="1c913-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c913-205">UC-appel RTC</span><span class="sxs-lookup"><span data-stu-id="1c913-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="1c913-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="1c913-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="1c913-207">2,95</span><span class="sxs-lookup"><span data-stu-id="1c913-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c913-208">UC-appel RTC</span><span class="sxs-lookup"><span data-stu-id="1c913-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="1c913-209">G-711</span><span class="sxs-lookup"><span data-stu-id="1c913-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="1c913-210">3,61</span><span class="sxs-lookup"><span data-stu-id="1c913-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1c913-211">Au-dessus ou au-dessus des activités d’analyse plus courantes, les tâches de maintenance doivent être exécutées pour les sites centraux, latéraux et succursales sur une base quotidienne, hebdomadaire et mensuelle, telle qu’elle est définie dans le Guide de fonctionnement de Lync RA.</span><span class="sxs-lookup"><span data-stu-id="1c913-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="1c913-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c913-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

