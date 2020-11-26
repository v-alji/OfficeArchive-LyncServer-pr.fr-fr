---
title: 'Lync Server 2013 : feuilles de calcul de sauvegarde et de restauration'
description: 'Lync Server 2013 : feuilles de calcul de sauvegarde et de restauration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437958"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="326fb-103">Sauvegarder et restaurer des feuilles de calcul pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="326fb-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="326fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="326fb-104">

<span> </span></span></span>

<span data-ttu-id="326fb-105">_**Dernière modification de la rubrique :** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="326fb-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="326fb-106">Le plan de sauvegarde et de restauration de votre organisation doit contenir des détails sur la façon dont et quand vous sauvegardez des données et des paramètres.</span><span class="sxs-lookup"><span data-stu-id="326fb-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="326fb-107">Vous pouvez utiliser les feuilles de calcul présentées ici pour documenter ces informations pour votre déploiement spécifique et pour les besoins en matière de sauvegarde et de restauration de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="326fb-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="326fb-108">Utilisez les feuilles de calcul suivantes pour enregistrer les informations dont vous avez besoin pour sauvegarder et restaurer des informations de base de données, de magasin de fichiers et de paramètres pour un pool de serveurs Lync ou un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="326fb-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="326fb-109">Conservation d’une ou plusieurs copies de ces feuilles de calcul dans un emplacement sécurisé de sorte qu’elles soient facilement accessibles si vous devez restaurer Lync Server.</span><span class="sxs-lookup"><span data-stu-id="326fb-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="326fb-110">Les feuilles de calcul de cette section couvrent uniquement les informations nécessaires pour restaurer les données et les paramètres des bases de données et serveurs Lync Server.</span><span class="sxs-lookup"><span data-stu-id="326fb-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="326fb-111">Si vous avez besoin de documenter d’autres informations de restauration, telles que les informations de réinstallation de systèmes d’exploitation et autres logiciels, utilisez les plans de déploiement de votre organisation ainsi que les plans de sauvegarde et de restauration pour répondre à ces exigences.</span><span class="sxs-lookup"><span data-stu-id="326fb-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="326fb-112">Feuille de calcul de sauvegarde et de restauration de base de données</span><span class="sxs-lookup"><span data-stu-id="326fb-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="326fb-113">Utilisez le tableau suivant pour enregistrer les informations dont vous avez besoin pour sauvegarder et restaurer des bases de données Lync Server.</span><span class="sxs-lookup"><span data-stu-id="326fb-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="326fb-114">Informations de base de données pour la sauvegarde et la restauration</span><span class="sxs-lookup"><span data-stu-id="326fb-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="326fb-115">Bases</span><span class="sxs-lookup"><span data-stu-id="326fb-115">Database</span></span></th>
<th><span data-ttu-id="326fb-116">Nom du serveur (FQDN)</span><span class="sxs-lookup"><span data-stu-id="326fb-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="326fb-117">Planning de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-117">Backup schedule</span></span></th>
<th><span data-ttu-id="326fb-118">Outil de sauvegarde de base de données</span><span class="sxs-lookup"><span data-stu-id="326fb-118">Database backup tool</span></span></th>
<th><span data-ttu-id="326fb-119">Jeu de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-119">Backup set</span></span></th>
<th><span data-ttu-id="326fb-120">Destination de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-120">Backup destination</span></span></th>
<th><span data-ttu-id="326fb-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="326fb-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="326fb-122">Base de données RTC sur le serveur principal pour les données utilisateur</span><span class="sxs-lookup"><span data-stu-id="326fb-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="326fb-123">Cmdlet <strong>Export-CsUserData</strong></span><span class="sxs-lookup"><span data-stu-id="326fb-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="326fb-124">Nommer</span><span class="sxs-lookup"><span data-stu-id="326fb-124">Name:</span></span></p>
<p><span data-ttu-id="326fb-125">Leur</span><span class="sxs-lookup"><span data-stu-id="326fb-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="326fb-126">Base de données LcsLog (nom par défaut) sur le serveur de base de données d’archivage</span><span class="sxs-lookup"><span data-stu-id="326fb-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="326fb-127">Outil de gestion SQL Server</span><span class="sxs-lookup"><span data-stu-id="326fb-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="326fb-128">Nommer</span><span class="sxs-lookup"><span data-stu-id="326fb-128">Name:</span></span></p>
<p><span data-ttu-id="326fb-129">Leur</span><span class="sxs-lookup"><span data-stu-id="326fb-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="326fb-130">Base de données LcsCdr sur analyse du serveur de base de données pour les enregistrements des détails des appels (CdR)</span><span class="sxs-lookup"><span data-stu-id="326fb-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="326fb-131">Outil de gestion SQL Server</span><span class="sxs-lookup"><span data-stu-id="326fb-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="326fb-132">Nommer</span><span class="sxs-lookup"><span data-stu-id="326fb-132">Name:</span></span></p>
<p><span data-ttu-id="326fb-133">Leur</span><span class="sxs-lookup"><span data-stu-id="326fb-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="326fb-134">Base de données QoEMetrics sur l’analyse des données d’un serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="326fb-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="326fb-135">Outil de gestion SQL Server</span><span class="sxs-lookup"><span data-stu-id="326fb-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="326fb-136">Nommer</span><span class="sxs-lookup"><span data-stu-id="326fb-136">Name:</span></span></p>
<p><span data-ttu-id="326fb-137">Leur</span><span class="sxs-lookup"><span data-stu-id="326fb-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="326fb-138">Base de données de conversation permanente</span><span class="sxs-lookup"><span data-stu-id="326fb-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="326fb-139">Outil de gestion SQL Server ou cmdlet <strong>Export-CsPersistentChatData</strong></span><span class="sxs-lookup"><span data-stu-id="326fb-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="326fb-140">Nommer</span><span class="sxs-lookup"><span data-stu-id="326fb-140">Name:</span></span></p>
<p><span data-ttu-id="326fb-141">Leur</span><span class="sxs-lookup"><span data-stu-id="326fb-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="326fb-142">Aucune sauvegarde ou restauration requise pour les bases de données suivantes :</span><span class="sxs-lookup"><span data-stu-id="326fb-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="326fb-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="326fb-143">Rtcdyn.</span></span> <span data-ttu-id="326fb-144">Les données utilisateur temporaires de cette base de données ne sont pas nécessaires à la restauration du service.</span><span class="sxs-lookup"><span data-stu-id="326fb-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="326fb-145">Rtcab.</span><span class="sxs-lookup"><span data-stu-id="326fb-145">Rtcab.</span></span> <span data-ttu-id="326fb-146">La base de données du carnet d’adresses est recréée automatiquement à partir de la liste d’adresses globale dans les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="326fb-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="326fb-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="326fb-147">Rgsdyn.</span></span> <span data-ttu-id="326fb-148">Il n’est pas nécessaire de restaurer les données du service de groupe de réponse temporaire dans cette base de données pour la restauration du service.</span><span class="sxs-lookup"><span data-stu-id="326fb-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="326fb-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="326fb-149">Cpsdyn.</span></span> <span data-ttu-id="326fb-150">Les informations dynamiques pour l’application de stationnement d’appel ne sont pas nécessaires pour la restauration du service.</span><span class="sxs-lookup"><span data-stu-id="326fb-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="326fb-151">MgcComp.</span><span class="sxs-lookup"><span data-stu-id="326fb-151">MgcComp.</span></span> <span data-ttu-id="326fb-152">La base de données de conformité pour la conversation permanente n’est pas nécessaire pour la restauration du service.</span><span class="sxs-lookup"><span data-stu-id="326fb-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="326fb-153">Feuille de calcul de sauvegarde et de restauration du magasin de fichiers</span><span class="sxs-lookup"><span data-stu-id="326fb-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="326fb-154">Utilisez le tableau suivant pour enregistrer les informations dont vous avez besoin pour sauvegarder et restaurer les magasins de fichiers.</span><span class="sxs-lookup"><span data-stu-id="326fb-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="326fb-155">Les magasins de fichiers contiennent des données telles que les métadonnées de contenu de la réunion, les journaux de mise à jour des mises à jour pour les mises à jour de l’appareil et les fichiers audio pour le groupe de réponse, le parc d’appels et les applications d’annonce.</span><span class="sxs-lookup"><span data-stu-id="326fb-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="326fb-156">Informations de stockage de fichiers pour la sauvegarde et la restauration</span><span class="sxs-lookup"><span data-stu-id="326fb-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="326fb-157">Contenu</span><span class="sxs-lookup"><span data-stu-id="326fb-157">Content</span></span></th>
<th><span data-ttu-id="326fb-158">Nom du serveur (FQDN)</span><span class="sxs-lookup"><span data-stu-id="326fb-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="326fb-159">Planning de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-159">Backup schedule</span></span></th>
<th><span data-ttu-id="326fb-160">Outil de sauvegarde du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="326fb-160">File system backup tool</span></span></th>
<th><span data-ttu-id="326fb-161">Partage de fichiers à sauvegarder \*</span><span class="sxs-lookup"><span data-stu-id="326fb-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="326fb-162">Destination de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-162">Backup destination</span></span></th>
<th><span data-ttu-id="326fb-163">Remarques</span><span class="sxs-lookup"><span data-stu-id="326fb-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="326fb-164">Magasin de fichiers de Lync Server</span><span class="sxs-lookup"><span data-stu-id="326fb-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="326fb-165">Outil de sauvegarde standard, tel que Robocopy</span><span class="sxs-lookup"><span data-stu-id="326fb-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="326fb-166">Sur le serveur de fichiers Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="326fb-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="326fb-167">Sur l’édition standard par défaut, pour le déploiement Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="326fb-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="326fb-168">En règle générale, un par site.</span><span class="sxs-lookup"><span data-stu-id="326fb-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="326fb-169">Les fichiers nommés <strong>réunion. actif</strong> ne doivent pas être sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="326fb-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="326fb-170">Ces fichiers sont utilisés et sont verrouillés lors d’une réunion.</span><span class="sxs-lookup"><span data-stu-id="326fb-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="326fb-171">Sauvegarder les paramètres et la feuille de calcul de restauration</span><span class="sxs-lookup"><span data-stu-id="326fb-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="326fb-172">Utilisez le tableau suivant pour enregistrer les informations dont vous avez besoin pour sauvegarder et restaurer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="326fb-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="326fb-173">Informations de paramètres pour la sauvegarde et la restauration</span><span class="sxs-lookup"><span data-stu-id="326fb-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="326fb-174">Bases</span><span class="sxs-lookup"><span data-stu-id="326fb-174">Database</span></span></th>
<th><span data-ttu-id="326fb-175">Nom du serveur (FQDN)</span><span class="sxs-lookup"><span data-stu-id="326fb-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="326fb-176">Planning de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-176">Backup schedule</span></span></th>
<th><span data-ttu-id="326fb-177">Outil de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-177">Backup tool</span></span></th>
<th><span data-ttu-id="326fb-178">Nom du fichier de configuration (. Xml)</span><span class="sxs-lookup"><span data-stu-id="326fb-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="326fb-179">Emplacement de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="326fb-179">Backup location</span></span></th>
<th><span data-ttu-id="326fb-180">Remarques</span><span class="sxs-lookup"><span data-stu-id="326fb-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="326fb-181">Base de données XDS dans le magasin central de gestion pour la configuration de la topologie (globale)</span><span class="sxs-lookup"><span data-stu-id="326fb-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="326fb-182">Cmdlet <strong>Export-CsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="326fb-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="326fb-183">Base de données lis dans le magasin central de gestion pour E9-1-1 informations d’emplacement (Global)</span><span class="sxs-lookup"><span data-stu-id="326fb-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="326fb-184">Cmdlet <strong>Export-CsLisConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="326fb-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="326fb-185">Base de données RgsConfig du serveur principal pour la configuration de Response Group (pool)</span><span class="sxs-lookup"><span data-stu-id="326fb-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="326fb-186">Cmdlet <strong>Export-CsRgsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="326fb-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="326fb-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="326fb-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

