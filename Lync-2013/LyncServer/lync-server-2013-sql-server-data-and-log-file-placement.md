---
title: 'Lync Server 2013 : Emplacement des fichiers journaux et des données SQL Server'
description: 'Lync Server 2013 : emplacement des données SQL Server et emplacement des fichiers journaux.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SQL Server data and log file placement
ms:assetid: 67aa525b-8aa3-474f-827e-8e1d4697f30f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398479(v=OCS.15)
ms:contentKeyID: 48184395
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a127254fec41a734136df9b63fc6cc8929745df7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444594"
---
# <a name="sql-server-data-and-log-file-placement-for-lync-server-2013"></a><span data-ttu-id="54814-103">Emplacement des fichiers journaux et des données SQL Server pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54814-103">SQL Server data and log file placement for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54814-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54814-104">

<span> </span></span></span>

<span data-ttu-id="54814-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="54814-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="54814-106">Lors de la planification et du déploiement de Microsoft SQL Server 2012 ou Microsoft SQL Server 2008 R2 SP1 pour votre pool frontal Lync Server 2013, il est important de tenir compte du placement des données et des fichiers journaux sur les disques durs physiques pour des performances.</span><span class="sxs-lookup"><span data-stu-id="54814-106">During the planning and deployment of Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2 SP1 for your Lync Server 2013 Front End pool, an important consideration is the placement of data and log files onto physical hard disks for performance.</span></span> <span data-ttu-id="54814-107">La configuration de disque recommandée consiste à implémenter un ensemble RAID de 1 + 0 avec 6 piles.</span><span class="sxs-lookup"><span data-stu-id="54814-107">The recommended disk configuration is to implement a 1+0 RAID set using 6 spindles.</span></span> <span data-ttu-id="54814-108">Le fait de placer tous les fichiers de base de données et les fichiers journaux qui sont utilisés par le pool frontal, et les rôles et services associés au serveur associé (c’est-à-dire, le service d’archivage et de surveillance, le service de groupe de réponse de Lync Server, le service de parc d’appels Lync Server) sur le jeu de disques RAID à l’aide de l’Assistant Déploiement de Lync</span><span class="sxs-lookup"><span data-stu-id="54814-108">Placing all database and log files that are used by the Front End pool and associated server roles and services (that is, Archiving and Monitoring Server, Lync Server Response Group service, Lync Server Call Park service) onto the RAID drive set using the Lync Server Deployment Wizard will result in a configuration that has been tested for good performance.</span></span> <span data-ttu-id="54814-109">Les fichiers de base de données et leurs responsables sont décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="54814-109">The database files and what they are responsible for is detailed in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="54814-110">Si vos stratégies et configurations SQL Server nécessitent une installation plus spécialisée, les fichiers de base de données et les fichiers journaux peuvent être installés vers tout emplacement prédéfini à l’aide de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="54814-110">If your policies and SQL Server configurations require a more specialized installation, the database and log files can be installed to any pre-defined location using the Lync Server Management Shell.</span></span> <span data-ttu-id="54814-111">Pour plus d’informations, voir <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">installation de la base de données à l’aide de Lync Server Management Shell dans Lync server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="54814-111">See <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">Database installation using Lync Server Management Shell in Lync Server 2013</A> for more details.</span></span>



</div>

### <a name="data-and-log-files-for-central-management-store"></a><span data-ttu-id="54814-112">Données et fichiers journaux pour le centre de gestion central</span><span class="sxs-lookup"><span data-stu-id="54814-112">Data and Log Files for Central Management Store</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54814-113">Fichiers de base de données du magasin de gestion centrale</span><span class="sxs-lookup"><span data-stu-id="54814-113">Central Management store database files</span></span></th>
<th><span data-ttu-id="54814-114">Fichier de données ou objet du journal</span><span class="sxs-lookup"><span data-stu-id="54814-114">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54814-115">XDS. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-115">Xds.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-116">Fichier journal des transactions du magasin de gestion central</span><span class="sxs-lookup"><span data-stu-id="54814-116">Transaction log file for the Central Management store</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-117">XDS. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-117">Xds.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-118">Conserve la configuration de la topologie Lync Server 2013 actuelle, telle que définie et publiée par le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="54814-118">Maintains the configuration of the current Lync Server 2013 topology, as defined and published by Topology Builder</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-119">Lis. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-119">Lis.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-120">Fichier de données de service d’information d’emplacement</span><span class="sxs-lookup"><span data-stu-id="54814-120">Location Information service data file</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-121">Lis. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-121">Lis.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-122">Journal des transactions pour le fichier de données du service d’information d’emplacement</span><span class="sxs-lookup"><span data-stu-id="54814-122">Transaction log for the Location Information service data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-user-conferencing-and-address-book"></a><span data-ttu-id="54814-123">Données et fichiers journaux pour l’utilisateur, les conférences et le carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="54814-123">Data and Log files for User, Conferencing, and Address Book</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54814-124">Fichiers de base de données principaux de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54814-124">Core Lync Server 2013 database files</span></span></th>
<th><span data-ttu-id="54814-125">Fichier de données ou objet du journal</span><span class="sxs-lookup"><span data-stu-id="54814-125">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54814-126">RTC. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-126">Rtc.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-127">Données utilisateur persistantes (telles que les listes de contrôle d’accès (ACL), les contacts, les conférences planifiées)</span><span class="sxs-lookup"><span data-stu-id="54814-127">Persistent user data (for example, access control lists (ACLs), contacts, scheduled conferences)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-128">RTC. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-128">Rtc.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-129">Journal des transactions pour les données RTC</span><span class="sxs-lookup"><span data-stu-id="54814-129">Transaction log for Rtc data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-130">RTCDyn. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-130">Rtcdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-131">Gère les données utilisateur temporaires (données d’exécution de la présence)</span><span class="sxs-lookup"><span data-stu-id="54814-131">Maintains transient user data (presence runtime data)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-132">RTCDyn. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-132">Rtcdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-133">Journal des transactions pour les données RTCDyn</span><span class="sxs-lookup"><span data-stu-id="54814-133">Transaction log for Rtcdyn data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-134">RTCAb. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-134">Rtcab.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-135">La base de données du carnet d’adresses RTC (Real-Time communications) est le référentiel SQL Server où sont stockés les informations de service de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="54814-135">Real-time communications (RTC) address book database is the SQL Server repository where Address Book service information is stored</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-136">RTCAb. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-136">Rtcab.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-137">Journal des transactions pour le service de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="54814-137">Transaction log for Address Book Service</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-138">Rtclocal. mdb</span><span class="sxs-lookup"><span data-stu-id="54814-138">Rtclocal.mdb</span></span></p></td>
<td><p><span data-ttu-id="54814-139">Héberge l’annuaire de conférences</span><span class="sxs-lookup"><span data-stu-id="54814-139">Hosts the conference directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-140">Rtcxds. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-140">Rtcxds.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-141">Conserve la sauvegarde des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54814-141">Maintains the backup for user data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-142">Rtcxds. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-142">Rtcxds.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-143">Journal des transactions pour les données Rtcxds</span><span class="sxs-lookup"><span data-stu-id="54814-143">Transaction log for Rtcxds data</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-call-park-and-response-group"></a><span data-ttu-id="54814-144">Données et fichiers journaux pour le parc d’appels et le groupe Response</span><span class="sxs-lookup"><span data-stu-id="54814-144">Data and Log Files for Call Park and Response Group</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54814-145">base de données d’applications</span><span class="sxs-lookup"><span data-stu-id="54814-145">Application database</span></span></th>
<th><span data-ttu-id="54814-146">Fichier de données ou objet du journal</span><span class="sxs-lookup"><span data-stu-id="54814-146">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54814-147">Cpsdyn. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-147">Cpsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-148">Base de données d’information dynamique pour l’application de parc d’appels</span><span class="sxs-lookup"><span data-stu-id="54814-148">Dynamic information database for the Call Park application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-149">Cpsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-149">Cpsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-150">Journal des transactions pour le fichier de données d’application de parc d’appels</span><span class="sxs-lookup"><span data-stu-id="54814-150">Transaction log for Call Park application data file</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-151">Rgsconfig. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-151">Rgsconfig.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-152">Fichier de données du service de groupe de réponse Lync Server pour la configuration des services</span><span class="sxs-lookup"><span data-stu-id="54814-152">Lync Server Response Group service data file for the configuration of the services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-153">Rgsconfig. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-153">Rgsconfig.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-154">Fichier journal des transactions pour la configuration de l’application Response Group</span><span class="sxs-lookup"><span data-stu-id="54814-154">Transaction log file for the Response Group application configuration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-155">Rgsdyn. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-155">Rgsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-156">Fichier de données du service Response Group pour les opérations d’exécution</span><span class="sxs-lookup"><span data-stu-id="54814-156">Response Group service data file for runtime operations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-157">Rgsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-157">Rgsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-158">Journal des transactions pour le fichier de données Runtime du service de Response Group</span><span class="sxs-lookup"><span data-stu-id="54814-158">Transaction log for the Response Group service runtime data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-archiving-and-monitoring-server"></a><span data-ttu-id="54814-159">Données et fichiers journaux pour le serveur d’archivage et de surveillance</span><span class="sxs-lookup"><span data-stu-id="54814-159">Data and Log Files for Archiving and Monitoring Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54814-160">Archivage et contrôle des fichiers de base de données</span><span class="sxs-lookup"><span data-stu-id="54814-160">Archiving and Monitoring database files</span></span></th>
<th><span data-ttu-id="54814-161">Fichier de données ou objet du journal</span><span class="sxs-lookup"><span data-stu-id="54814-161">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54814-162">LcsCdr. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-162">LcsCdr.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-163">Magasin de données pour le processus d’enregistrement des détails des appels (CDR) du serveur de surveillance</span><span class="sxs-lookup"><span data-stu-id="54814-163">Data store for the call detail recording (CDR) process of the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-164">LcsCdr. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-164">LcsCdr.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-165">Journal des transactions pour les données d’enregistrement des détails des appels (CDR)</span><span class="sxs-lookup"><span data-stu-id="54814-165">Transaction log for call detail recording (CDR) data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-166">QoEMetrics. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-166">QoEMetrics.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-167">Fichier de données de qualité de l’utilisateur stocké à partir du serveur de surveillance</span><span class="sxs-lookup"><span data-stu-id="54814-167">Quality of Experience data file stored from the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-168">QoEMetrics. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-168">QoEMetrics.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-169">Journal des transactions d’analyse des données</span><span class="sxs-lookup"><span data-stu-id="54814-169">Transaction log for Monitoring data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54814-170">LcsLog. mdf</span><span class="sxs-lookup"><span data-stu-id="54814-170">Lcslog.mdf</span></span></p></td>
<td><p><span data-ttu-id="54814-171">Fichier de données pour la conservation des données de messagerie instantanée et de conférence sur un serveur d’archivage</span><span class="sxs-lookup"><span data-stu-id="54814-171">Data file for the retention of instant messaging and conferencing data on an Archiving Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54814-172">LcsLog. ldf</span><span class="sxs-lookup"><span data-stu-id="54814-172">Lcslog.ldf</span></span></p></td>
<td><p><span data-ttu-id="54814-173">Journal des transactions d’archivage des données</span><span class="sxs-lookup"><span data-stu-id="54814-173">Transaction log for Archiving data</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="54814-174">Dans cette rubrique, les références sont prises sur le disque et sur le jeu RAID.</span><span class="sxs-lookup"><span data-stu-id="54814-174">In this topic, references are made to disk and to RAID set.</span></span> <span data-ttu-id="54814-175">Notez que dans la configuration des ressources SQL Server, le fait de faire référence à un disque correspond à un seul appareil matériel.</span><span class="sxs-lookup"><span data-stu-id="54814-175">Note that in the configuration of SQL Server resources, referring to a disk means a single hardware device.</span></span> <span data-ttu-id="54814-176">Un disque dur doté de deux partitions, l’un contenant les fichiers journaux et l’autre partition contenant les fichiers de données, n’est pas le même que sur deux disques.</span><span class="sxs-lookup"><span data-stu-id="54814-176">A hard disk drive with two partitions, one holding log files and the other partition holding data files, is not the same as two disks, each dedicated to either log or data files.</span></span>

<span data-ttu-id="54814-177">En ce qui concerne les jeux RAID, il existe plusieurs technologies RAID différentes de celles de différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="54814-177">In reference to RAID sets, there are a number of different RAID technologies from various vendors.</span></span> <span data-ttu-id="54814-178">Par le biais de la prolifération des réseaux de zone de stockage, les jeux RAID dédiés à un seul système sont plus rares.</span><span class="sxs-lookup"><span data-stu-id="54814-178">And, with the proliferation of storage area networks (SAN), RAID sets dedicated to a single system are rarer.</span></span> <span data-ttu-id="54814-179">Vous devez consulter votre fabricant de réseau ou de réseau pour déterminer la configuration qui correspond le mieux à votre disposition de disque lorsque vous configurez des performances SQL Server avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54814-179">You should consult with your RAID or SAN vendor to determine what the best configuration is for your disk layout when configuring for SQL Server performance with Lync Server 2013.</span></span>

<span data-ttu-id="54814-180">Notez également que tous les lecteurs de disque ne sont pas créés de la même manière ; d’autres sont plus performantes que d’autres.</span><span class="sxs-lookup"><span data-stu-id="54814-180">Note also that not all disk drives are created equally; some perform better than others.</span></span> <span data-ttu-id="54814-181">Même les lecteurs du même fabricant peuvent varier en fonction de la vitesse de rotation, de la taille du cache matériel et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="54814-181">Even drives from the same manufacturer can vary in performance because of rotational speed, hardware cache size, and other factors.</span></span>

<span data-ttu-id="54814-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54814-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

