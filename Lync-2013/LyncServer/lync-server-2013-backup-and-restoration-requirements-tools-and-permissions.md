---
title: 'Lync Server 2013 : configuration requise pour la sauvegarde et la restauration : outils et autorisations'
description: 'Lync Server 2013 : configuration requise pour la sauvegarde et la restauration : outils et autorisations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437979"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="37b7b-103">Configurations requises pour la sauvegarde et la restauration dans Lync Server 2013 : outils et autorisations</span><span class="sxs-lookup"><span data-stu-id="37b7b-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37b7b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37b7b-104">

<span> </span></span></span>

<span data-ttu-id="37b7b-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="37b7b-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="37b7b-106">Cette rubrique identifie les outils que vous pouvez utiliser pour sauvegarder et restaurer Lync Server 2013, les autorisations dont vous avez besoin et si vous pouvez exécuter des commandes à distance ou localement.</span><span class="sxs-lookup"><span data-stu-id="37b7b-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="37b7b-107">Ce sujet décrit en particulier les outils fournis avec Lync Server pour la sauvegarde et la restauration.</span><span class="sxs-lookup"><span data-stu-id="37b7b-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="37b7b-108">Sauvegardes</span><span class="sxs-lookup"><span data-stu-id="37b7b-108">Backups</span></span>

<span data-ttu-id="37b7b-109">Pour sauvegarder Lync Server, utilisez les outils identifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="37b7b-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="37b7b-110">Toutes les commandes dont vous avez besoin pour sauvegarder Lync Server peuvent être rédigées en scripts et peuvent être exécutées à distance.</span><span class="sxs-lookup"><span data-stu-id="37b7b-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="37b7b-111">Outils de sauvegarde de Lync Server</span><span class="sxs-lookup"><span data-stu-id="37b7b-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b7b-112">Pour sauvegarder ce problème, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="37b7b-112">To back up this:</span></span></th>
<th><span data-ttu-id="37b7b-113">Utilisez cet outil ou cette applet de applet :</span><span class="sxs-lookup"><span data-stu-id="37b7b-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-114">Données de configuration topologique (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-116">Données du service d’information d’emplacement (E9-1-1) (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-118">Données de configuration de Response Group (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-120">Données utilisateur persistantes (base de données Rtcxds. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="37b7b-121">ID de conférence</span><span class="sxs-lookup"><span data-stu-id="37b7b-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="37b7b-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="37b7b-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="37b7b-123">Archivage de la base de données (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="37b7b-124">Surveillance de la base de données d’enregistrement des détails des appels (LcsCDR. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="37b7b-125">Surveillance de la base de données QoE (QoEMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="37b7b-126">Outil de base de données SQL Server, tel que SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="37b7b-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-127">Base de données de discussions permanentes (MGC. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-128">Procédures de sauvegarde SQL Server ou Export-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="37b7b-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="37b7b-129">Export-CsPersistentChatData exporter les données d’une conversation permanente sous forme de fichier.</span><span class="sxs-lookup"><span data-stu-id="37b7b-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-130">Tous les magasins de fichiers : magasin de fichiers Lync Server et magasin de fichiers d’archivage</span><span class="sxs-lookup"><span data-stu-id="37b7b-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="37b7b-131">Les fichiers nommés <STRONG>réunion. actif</STRONG> ne doivent pas être sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="37b7b-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="37b7b-132">Ces fichiers sont utilisés et verrouillés lors d’une réunion.</span><span class="sxs-lookup"><span data-stu-id="37b7b-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="37b7b-133">Outil standard de gestion du système de fichiers, tel que Robocopy.</span><span class="sxs-lookup"><span data-stu-id="37b7b-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="37b7b-134">Répétition</span><span class="sxs-lookup"><span data-stu-id="37b7b-134">Restoration</span></span>

<span data-ttu-id="37b7b-135">Pour restaurer Lync Server, utilisez les outils figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="37b7b-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="37b7b-136">Toutes les commandes dont vous avez besoin pour restaurer Lync Server peuvent être scripts.</span><span class="sxs-lookup"><span data-stu-id="37b7b-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="37b7b-137">Certains peuvent être exécutés à distance, mais d’autres doivent être exécutés localement, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="37b7b-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="37b7b-138">Outils de restauration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="37b7b-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b7b-139">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="37b7b-139">To do this:</span></span></th>
<th><span data-ttu-id="37b7b-140">Utilisez cet outil ou cette applet de applet :</span><span class="sxs-lookup"><span data-stu-id="37b7b-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-141">Créer un nouvel ordinateur ou nettoyer votre ordinateur</span><span class="sxs-lookup"><span data-stu-id="37b7b-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="37b7b-142">Programme d’installation du système d’exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="37b7b-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="37b7b-143">Programme d’installation de SQL Server</span><span class="sxs-lookup"><span data-stu-id="37b7b-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="37b7b-144">Composant logiciel enfichable Certificats de la console de gestion des certificats, si vous restaurez des certificats à l’aide d’une clé privée exportable</span><span class="sxs-lookup"><span data-stu-id="37b7b-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-145">Restaurer les données du magasin de fichiers</span><span class="sxs-lookup"><span data-stu-id="37b7b-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="37b7b-146">Outil standard de gestion du système de fichiers, tel que Robocopy</span><span class="sxs-lookup"><span data-stu-id="37b7b-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-147">Recréer des bases de données vides et définir des autorisations pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="37b7b-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="37b7b-148">magasin central de gestion</span><span class="sxs-lookup"><span data-stu-id="37b7b-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="37b7b-149">serveur principal</span><span class="sxs-lookup"><span data-stu-id="37b7b-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="37b7b-150">base de données de surveillance</span><span class="sxs-lookup"><span data-stu-id="37b7b-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="37b7b-151">base de données d’archivage</span><span class="sxs-lookup"><span data-stu-id="37b7b-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="37b7b-152">Install-CsDatabase</span><span class="sxs-lookup"><span data-stu-id="37b7b-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-153">Restaurer le pointeur services de domaine Active Directory (AD FS) vers le magasin de gestion central</span><span class="sxs-lookup"><span data-stu-id="37b7b-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="37b7b-154">Si vous perdez le point de connexion de service à tout moment, vous pouvez réexécuter cette cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b7b-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="37b7b-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="37b7b-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-156">Importer les paramètres de topologie, de stratégie et de configuration dans le magasin de gestion central (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-158">Publier et activer la topologie</span><span class="sxs-lookup"><span data-stu-id="37b7b-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="37b7b-159">Générateur de topologie</span><span class="sxs-lookup"><span data-stu-id="37b7b-159">Topology Builder</span></span></p>
<p><span data-ttu-id="37b7b-160">ou</span><span class="sxs-lookup"><span data-stu-id="37b7b-160">-or-</span></span></p>
<p><span data-ttu-id="37b7b-161">Publish-CsTopology et Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="37b7b-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-162">Activer la dernière topologie publiée</span><span class="sxs-lookup"><span data-stu-id="37b7b-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="37b7b-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="37b7b-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-164">Réinstaller les composants du serveur Lync</span><span class="sxs-lookup"><span data-stu-id="37b7b-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="37b7b-165">Configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="37b7b-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="37b7b-166">Situés dans le dossier d’installation ou le média de Lync Server sur \setup\amd64\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="37b7b-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-167">Restaurer des informations d’emplacement (E9-1-1) (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-169">Restaurer des données utilisateur persistantes (Rtcxds. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="37b7b-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-171">Restauration des données de configuration de Response Group (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="37b7b-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="37b7b-173">Si la configuration est restaurée dans un nouveau pool déployé qui ne possède pas de données de groupe de réponse dans la base de données, vous devez utiliser l’option – OverwriteOwner.</span><span class="sxs-lookup"><span data-stu-id="37b7b-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="37b7b-174">Utilisez cette option même si les données en cours de restauration se trouvent dans un pool portant le même nom de domaine complet (FQDN).</span><span class="sxs-lookup"><span data-stu-id="37b7b-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="37b7b-175">Dans le cas contraire, l’importation échoue en raison des objets de contact dans les groupes de réponse déjà présents dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37b7b-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b7b-176">Restaurez les bases de données suivantes :</span><span class="sxs-lookup"><span data-stu-id="37b7b-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="37b7b-177">Archivage de la base de données (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="37b7b-178">Surveiller des bases de données : base de données d’enregistrement des détails des appels (LcsCDR. mdf) et base de données QoE (QoEMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="37b7b-179">Outils de gestion de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="37b7b-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b7b-180">Base de données de discussions permanentes (MGS. mdf)</span><span class="sxs-lookup"><span data-stu-id="37b7b-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="37b7b-181">Procédures de restauration SQL Server ou Import-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="37b7b-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="37b7b-182">Vous pouvez utiliser des Import-CsPersistentChatData avec un fichier créé par Export-CsPersistentChatData et les données seront importées dans la base de données de chat persistant.</span><span class="sxs-lookup"><span data-stu-id="37b7b-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="37b7b-183">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="37b7b-183">Required Permissions</span></span>

<span data-ttu-id="37b7b-184">Les utilisateurs doivent être membres du groupe **RTCUniversalServerAdmins** pour effectuer toutes les commandes décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="37b7b-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="37b7b-185">La plupart des commandes de sauvegarde et de restauration ne prennent pas en charge le contrôle d’accès basé sur les rôles (RBAC).</span><span class="sxs-lookup"><span data-stu-id="37b7b-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="37b7b-186">Les applets de contrôle de chat permanent Export-CsPersistentChatData et Import-CsPersistentChatData doivent être exécutés par un utilisateur membre du groupe CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="37b7b-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="37b7b-187">Pour exécuter l’Assistant Déploiement de Lync Server, un utilisateur doit également être membre du groupe administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="37b7b-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="37b7b-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37b7b-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

