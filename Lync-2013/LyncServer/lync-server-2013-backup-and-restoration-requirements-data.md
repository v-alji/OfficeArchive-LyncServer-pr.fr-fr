---
title: 'Lync Server 2013 : configuration requise pour la sauvegarde et la restauration : données'
description: 'Lync Server 2013 : configuration requise pour la sauvegarde et la restauration : données.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437986"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="bd519-103">Configuration requise pour la sauvegarde et la restauration dans Lync Server 2013 : données</span><span class="sxs-lookup"><span data-stu-id="bd519-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd519-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd519-104">

<span> </span></span></span>

<span data-ttu-id="bd519-105">_**Dernière modification de la rubrique :** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="bd519-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="bd519-106">Lync Server utilise les paramètres et les informations de configuration stockées dans les bases de données et les données qui sont stockées dans les bases de données et les magasins de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bd519-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="bd519-107">Cette rubrique décrit les données que vous devez sauvegarder pour pouvoir restaurer le service en cas d’échec ou d’interruption de votre organisation, ainsi que les données et composants utilisés par Lync Server et dont vous avez besoin pour vous sauvegarder séparément.</span><span class="sxs-lookup"><span data-stu-id="bd519-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="bd519-108">Paramètres et configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd519-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="bd519-109">Cette rubrique inclut les procédures de sauvegarde et de restauration des paramètres et des informations de configuration nécessaires à la récupération du service Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="bd519-110">Les informations de configuration se trouvent dans le magasin de gestion central ou sur une autre base de données principale ou sur un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="bd519-111">Le tableau suivant répertorie les paramètres et les informations de configuration nécessaires pour la sauvegarde et la restauration.</span><span class="sxs-lookup"><span data-stu-id="bd519-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="bd519-112">Paramètres et données de configuration</span><span class="sxs-lookup"><span data-stu-id="bd519-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd519-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="bd519-113">Type of data</span></span></th>
<th><span data-ttu-id="bd519-114">Emplacement de stockage</span><span class="sxs-lookup"><span data-stu-id="bd519-114">Where stored</span></span></th>
<th><span data-ttu-id="bd519-115">Description/moment de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="bd519-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd519-116">Informations de configuration de la topologie</span><span class="sxs-lookup"><span data-stu-id="bd519-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="bd519-117">Magasin de gestion centralisée (base de données : XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="bd519-118">Paramètres de topologie, de stratégie et de configuration.</span><span class="sxs-lookup"><span data-stu-id="bd519-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="bd519-119">Sauvegardez vos sauvegardes régulières et après avoir utilisé le panneau de configuration ou les applets de commande Lync Server pour modifier votre configuration ou vos stratégies.</span><span class="sxs-lookup"><span data-stu-id="bd519-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd519-120">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="bd519-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="bd519-121">Magasin de gestion centralisée (base de données : lis. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="bd519-122">Informations de configuration de 9-1-1 voix entreprise améliorée (E9-1-1).</span><span class="sxs-lookup"><span data-stu-id="bd519-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="bd519-123">Ces informations sont généralement statiques.</span><span class="sxs-lookup"><span data-stu-id="bd519-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="bd519-124">Sauvegardez vos sauvegardes régulières.</span><span class="sxs-lookup"><span data-stu-id="bd519-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd519-125">Informations de configuration du groupe de réponse</span><span class="sxs-lookup"><span data-stu-id="bd519-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="bd519-126">Serveur principal ou Standard Edition Server (base de données : RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="bd519-127">Response Group Group agent, files d’attente et flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bd519-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="bd519-128">Sauvegardez vos sauvegardes régulières et après avoir ajouté ou modifié des groupes d’agents, des files d’attente ou des flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bd519-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="bd519-129">Exigences en matière de données</span><span class="sxs-lookup"><span data-stu-id="bd519-129">Data Requirements</span></span>

<span data-ttu-id="bd519-130">Vous trouverez ci-dessous la liste des données du serveur Lync dont vous avez besoin pour vous permettre de restaurer le service Lync Server en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="bd519-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="bd519-131">Notez que certains types de données ne sont pas nécessaires pour la récupération.</span><span class="sxs-lookup"><span data-stu-id="bd519-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="bd519-132">Cette rubrique ne contient pas de procédures pour la sauvegarde de ces types de données, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd519-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="bd519-133">Des données utilisateur temporaires, telles que des points de terminaison et des abonnements, des serveurs de conférence actifs et des États de conférence temporaire (base de données : RtcDyn. mdf);</span><span class="sxs-lookup"><span data-stu-id="bd519-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="bd519-134">Données du carnet d’adresses (bases de données : RTCAb. mdf et Rtcab1. mdf).</span><span class="sxs-lookup"><span data-stu-id="bd519-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="bd519-135">La base de données du carnet d’adresses est automatiquement générée à partir des services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bd519-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="bd519-136">Informations dynamiques pour l’application de parc d’appels (base de données : CpsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="bd519-137">Données de groupe de réponse passagère, telles que l’état de connexion d’un agent et les informations d’attente d’appel (base de données : RgsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="bd519-138">La base de données de conformité pour les discussions permanentes (base de données : MgcComp. mdf).</span><span class="sxs-lookup"><span data-stu-id="bd519-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="bd519-139">Si la conformité des conversations permanentes est activée, les informations contenues dans la base de données de compatibilité des conversations permanentes sont temporaires tant qu’un adaptateur est configuré pour lire des informations de la base de données et le convertir dans un autre format.</span><span class="sxs-lookup"><span data-stu-id="bd519-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="bd519-140">Par conséquent, la base de données de conformité d’une conversation permanente est considérée comme temporaire.</span><span class="sxs-lookup"><span data-stu-id="bd519-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="bd519-141">Lync Server 2013 permanent Chat Server est fourni avec un adaptateur XML.</span><span class="sxs-lookup"><span data-stu-id="bd519-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="bd519-142">Vous pouvez également installer des adaptateurs personnalisés qui prennent ces données et les déplacer vers d’autres sources, telles que des archives hébergées d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="bd519-143">Le tableau suivant identifie les données que vous devez sauvegarder et restaurer.</span><span class="sxs-lookup"><span data-stu-id="bd519-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="bd519-144">Données stockées dans des bases de données</span><span class="sxs-lookup"><span data-stu-id="bd519-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd519-145">Type de données</span><span class="sxs-lookup"><span data-stu-id="bd519-145">Type of data</span></span></th>
<th><span data-ttu-id="bd519-146">Emplacement de stockage</span><span class="sxs-lookup"><span data-stu-id="bd519-146">Where stored</span></span></th>
<th><span data-ttu-id="bd519-147">Description/moment de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="bd519-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd519-148">Données utilisateur persistantes</span><span class="sxs-lookup"><span data-stu-id="bd519-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="bd519-149">Serveur principal ou Standard Edition Server (base de données : RTCXDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="bd519-150">Droits d’utilisateur, listes des contacts utilisateur, données du serveur ou du pool, conférences planifiées, etc.</span><span class="sxs-lookup"><span data-stu-id="bd519-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="bd519-151">Les données utilisateur n’incluent pas le contenu chargé dans une conférence.</span><span class="sxs-lookup"><span data-stu-id="bd519-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="bd519-152">Sauvegardez vos sauvegardes régulières.</span><span class="sxs-lookup"><span data-stu-id="bd519-152">Back up with your regular backups.</span></span> <span data-ttu-id="bd519-153">Ces informations sont dynamiques, mais la perte des mises à jour n’est pas irrémédiablement apportée à Lync Server si vous avez besoin de procéder à la restauration de votre dernière sauvegarde normale.</span><span class="sxs-lookup"><span data-stu-id="bd519-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="bd519-154">Si les listes de contacts sont essentielles pour votre organisation, vous pouvez sauvegarder ces données plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="bd519-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd519-155">Archivage de données</span><span class="sxs-lookup"><span data-stu-id="bd519-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="bd519-156">Archivage de la base de données (base de données : LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="bd519-157">Ces données peuvent être stockées sur Exchange 2013, si vous avez activé l’option d’intégration de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="bd519-158">Dans le cas contraire, il s’agit d’une base de données d’archivage Lync Server, qui peut être colocalisée avec une autre base de données Lync Server ou autonome sur un serveur de base de données distinct.</span><span class="sxs-lookup"><span data-stu-id="bd519-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="bd519-159">Messagerie instantanée et contenu de la réunion.</span><span class="sxs-lookup"><span data-stu-id="bd519-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="bd519-160">Cette information n’est pas essentielle pour Lync Server, mais elle peut être essentielle pour les fins réglementaires de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bd519-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="bd519-161">Déterminez votre planning de sauvegarde en conséquence.</span><span class="sxs-lookup"><span data-stu-id="bd519-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd519-162">Surveiller les données</span><span class="sxs-lookup"><span data-stu-id="bd519-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="bd519-163">Surveiller des bases de données (LcsCDR. mdf et QoeMetrics. mdf)</span><span class="sxs-lookup"><span data-stu-id="bd519-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="bd519-164">Ces bases de données risquent d’être colocalisées avec une autre base de données Lync Server ou autonome sur un serveur de base de données distinct.</span><span class="sxs-lookup"><span data-stu-id="bd519-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="bd519-165">Les enregistrements des détails des appels (LcsCDR. mdf) et la qualité de l’expertise (QoE) (QoeMetrics. mdf).</span><span class="sxs-lookup"><span data-stu-id="bd519-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="bd519-166">Les enregistrements des détails des appels sont dynamiques et peuvent être importants pour votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="bd519-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="bd519-167">Déterminez votre planning de sauvegarde en tenant compte de l’utilisation de ces enregistrements pour des raisons réglementaires.</span><span class="sxs-lookup"><span data-stu-id="bd519-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="bd519-168">Les informations sur la qualité de l’expérimentation sont dynamiques.</span><span class="sxs-lookup"><span data-stu-id="bd519-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="bd519-169">La perte de données QoE n’est pas essentielle pour l’opération de Lync Server, mais elle peut être essentielle pour votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="bd519-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="bd519-170">Déterminez votre planning de sauvegarde en fonction de la façon dont ces informations sont importantes pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bd519-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd519-171">Données de chat permanent</span><span class="sxs-lookup"><span data-stu-id="bd519-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="bd519-172">Base de données de chat permanent (MGD. mdf).</span><span class="sxs-lookup"><span data-stu-id="bd519-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="bd519-173">Cette base de données est susceptible d’être colocalisée avec une autre base de données Lync Server ou indépendante sur un serveur de base de données distinct.</span><span class="sxs-lookup"><span data-stu-id="bd519-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="bd519-174">Les données de conversation permanente sont des messages de discussion en cours de publication dans des salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="bd519-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="bd519-175">Il s’agit souvent de données critiques pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="bd519-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="bd519-176">Vous pouvez choisir d’utiliser la sauvegarde SQL Server ou exporter la base de données à l’aide de l’applet de passe <strong>Export-CsPersistentChatData</strong> fournie dans Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="bd519-177">Pour la récupération des données, vous pouvez importer et restaurer la base de données à l’emplacement de la dernière sauvegarde complète, ce qui signifie que vous ne pouvez pas restaurer la base de données vers le point de défaillance.</span><span class="sxs-lookup"><span data-stu-id="bd519-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="bd519-178">Exigences relatives aux données du magasin de fichiers</span><span class="sxs-lookup"><span data-stu-id="bd519-178">File Store Data Requirements</span></span>

<span data-ttu-id="bd519-179">Dans un déploiement Enterprise Edition, le magasin de fichiers de Lync Server se trouve généralement sur un serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bd519-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="bd519-180">Dans un déploiement Standard Edition, le magasin de fichiers de Lync Server se trouve par défaut sur le serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="bd519-181">En règle générale, il existe un magasin de fichiers Lync Server partagé pour un site.</span><span class="sxs-lookup"><span data-stu-id="bd519-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="bd519-182">Le magasin de fichiers permanents chat utilise le même partage de fichiers que le magasin de fichiers du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="bd519-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="bd519-183">Les emplacements du magasin de fichiers sont identifiés par le \\ \\ nom de partage du serveur \\ .</span><span class="sxs-lookup"><span data-stu-id="bd519-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="bd519-184">Pour trouver les emplacements spécifiques de vos magasins de fichiers, ouvrez le générateur de topologie et recherchez dans le nœud **magasins de fichiers** .</span><span class="sxs-lookup"><span data-stu-id="bd519-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="bd519-185">Le tableau suivant identifie les banques de fichiers que vous devez sauvegarder et restaurer.</span><span class="sxs-lookup"><span data-stu-id="bd519-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="bd519-186">Magasins de fichiers</span><span class="sxs-lookup"><span data-stu-id="bd519-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd519-187">Type de données</span><span class="sxs-lookup"><span data-stu-id="bd519-187">Type of data</span></span></th>
<th><span data-ttu-id="bd519-188">Emplacement de stockage</span><span class="sxs-lookup"><span data-stu-id="bd519-188">Where stored</span></span></th>
<th><span data-ttu-id="bd519-189">Description/moment de la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="bd519-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd519-190">Magasin de fichiers de Lync Server</span><span class="sxs-lookup"><span data-stu-id="bd519-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="bd519-191">Généralement sur un serveur de fichiers, un groupe de fichiers ou un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="bd519-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="bd519-192">Le contenu de la réunion, les métadonnées de contenu de la réunion, les journaux de conformité des réunions, les fichiers de données d’application, les fichiers de mise à jour des mises à jour de périphériques, les fichiers audio pour les réunions de groupe de réponse</span><span class="sxs-lookup"><span data-stu-id="bd519-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="bd519-193">Sauvegardez vos sauvegardes régulières.</span><span class="sxs-lookup"><span data-stu-id="bd519-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="bd519-194">Exigences de sauvegarde supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bd519-194">Additional Backup Requirements</span></span>

<span data-ttu-id="bd519-195">Pour vous aider à garantir la possibilité de restaurer les services Lync Server en cas d’échec, vous devez sauvegarder les composants nécessaires qui ne font pas partie de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="bd519-196">Les composants suivants ne sont pas sauvegardés ou restaurés dans le cadre du processus de sauvegarde et de restauration de Lync Server décrits dans ce document :</span><span class="sxs-lookup"><span data-stu-id="bd519-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="bd519-197">**Services de domaine Active Directory**   Pour sauvegarder les services de domaine Active Directory (AD DS), vous devez utiliser les outils Active Directory en même temps que Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="bd519-198">Il est important de maintenir la synchronisation AD DS sur Lync Server, afin d’éviter les problèmes qui peuvent survenir lorsque Lync Server attend des objets de contact qui ne correspondent pas à ceux d’AD DS.</span><span class="sxs-lookup"><span data-stu-id="bd519-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="bd519-199">AD DS stocke les paramètres suivants qui sont utilisés par Lync Server :</span><span class="sxs-lookup"><span data-stu-id="bd519-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="bd519-200">URI SIP utilisateur et autres paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd519-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="bd519-201">Objets de contact pour des applications telles que Response Group et attendant.</span><span class="sxs-lookup"><span data-stu-id="bd519-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="bd519-202">Pointeur vers le magasin de gestion central.</span><span class="sxs-lookup"><span data-stu-id="bd519-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="bd519-203">Compte d’authentification Kerberos (objet ordinateur facultatif) et groupes de sécurité Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="bd519-204">Pour plus d’informations sur l’utilisation de la fonction de sauvegarde et de restauration des services AD DS dans Windows Server 2008, voir le guide étape par étape de sauvegarde et récupération AD DS à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) .</span><span class="sxs-lookup"><span data-stu-id="bd519-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="bd519-205">**Autorités de certification et certificats**   Utilisez la stratégie de votre organisation pour sauvegarder vos certificats d’autorité de certification et de certification.</span><span class="sxs-lookup"><span data-stu-id="bd519-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="bd519-206">Si vous utilisez des clés privées exportables, vous pouvez sauvegarder le certificat et la clé privée, puis les exporter si vous suivez les procédures décrites dans ce document pour restaurer Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="bd519-207">Si vous utilisez une autorité de certification interne, vous pouvez procéder de nouveau à l’inscription si vous avez besoin de restaurer Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="bd519-208">Il est important que vous conserviez la clé privée à un emplacement sécurisé pour qu’elle soit disponible en cas d’échec d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd519-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="bd519-209">**System Center Operations Manager**   Si vous utilisez Microsoft System Center Operations Manager (auparavant Microsoft Operations Manager) pour surveiller votre déploiement de Lync Server, vous pouvez éventuellement sauvegarder les données qu’il crée lors de l’analyse de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="bd519-210">Utilisez votre processus de sauvegarde SQL Server standard pour sauvegarder les fichiers System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="bd519-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="bd519-211">Ces fichiers ne sont pas restaurés lors de la récupération.</span><span class="sxs-lookup"><span data-stu-id="bd519-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="bd519-212">**Configuration de la passerelle de réseau téléphonique commuté (PSTN)**   Si vous utilisez des appareils de succursale voix entreprise ou Survivables, vous devez sauvegarder la configuration de la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="bd519-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="bd519-213">Pour plus d’informations sur la sauvegarde et la restauration des configurations de passerelle RTC, consultez votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bd519-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="bd519-214">**Versions et coexistence de Lync Server ou du serveur Office Communications Server**   Si le déploiement de Lync Server 2013 est le même que celui de Lync Server 2010 ou d’une version antérieure de Microsoft Office Communications Server, vous ne pouvez pas utiliser les procédures décrites dans ce document pour sauvegarder ou restaurer la version antérieure.</span><span class="sxs-lookup"><span data-stu-id="bd519-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="bd519-215">À la place, vous devez utiliser les procédures de sauvegarde et de restauration indiquées spécifiquement pour votre version antérieure.</span><span class="sxs-lookup"><span data-stu-id="bd519-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="bd519-216">Pour plus d’informations sur la sauvegarde et la restauration de Lync Server 2010, voir [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span><span class="sxs-lookup"><span data-stu-id="bd519-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="bd519-217">Pour plus d’informations sur la sauvegarde et la restauration de Microsoft Office Communications Server 2007 R2, voir [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) .</span><span class="sxs-lookup"><span data-stu-id="bd519-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="bd519-218">**Informations sur l’infrastructure**   Vous devez sauvegarder des informations sur votre infrastructure, telles que la configuration de votre pare-feu, la configuration de l’équilibrage de charge, la configuration d’Internet Information Services (IIS), les enregistrements DNS et les adresses IP et la configuration du protocole DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="bd519-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="bd519-219">Pour plus d’informations sur la sauvegarde de ces composants, contactez leurs fournisseurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="bd519-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="bd519-220">**Microsoft Exchange et Exchange Unified Messaging (um)**   Sauvegardez et restaurez Microsoft Exchange et Exchange UM comme décrit dans la documentation Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="bd519-221">Pour plus d’informations sur la sauvegarde et la restauration d’Exchange Server 2013, voir [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) .</span><span class="sxs-lookup"><span data-stu-id="bd519-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="bd519-222">Pour plus d’informations sur la sauvegarde et la restauration d’Exchange Server 2010, voir [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) .</span><span class="sxs-lookup"><span data-stu-id="bd519-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="bd519-223">Notez que Lync Server 2013 offre la possibilité d’utiliser les listes de contacts de l’utilisateur, les photos haute définition et les données d’archivage stockées dans Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="bd519-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="bd519-224">Pour plus d’informations sur la sauvegarde de ces types de données, consultez la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="bd519-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="bd519-225">Les **photos haute définition** sont sauvegardées dans le cadre de la sauvegarde du serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="bd519-226">Le **magasin de contacts unifié** est présenté dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bd519-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="bd519-227">Un magasin de contacts unifié permet aux utilisateurs de conserver toutes leurs informations de contact dans Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="bd519-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="bd519-228">Assurez-vous que les sauvegardes sont à jour pour les utilisateurs en termes de stockage ou de gestion des contacts de l’utilisateur dans le magasin de contacts unifié ou sur le serveur principal Lync.</span><span class="sxs-lookup"><span data-stu-id="bd519-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="bd519-229">Les scénarios suivants vous montrent où la migration de contacts utilisateur vers le magasin de contacts unifié peut provoquer des problèmes pour le processus de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="bd519-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="bd519-230">**Scénario 1 :** Les contacts des utilisateurs sont déplacés vers le magasin de contacts unifié, et une restauration est effectuée à partir d’une sauvegarde de serveur Lync prélevée avant la migration des contacts utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bd519-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="bd519-231">Dans ce scénario, l’utilisateur aura un état de contacts obsolètes jusqu’à un jour jusqu’à ce que la tâche de migration de Lync Server commence à migrer les contacts de l’utilisateur vers Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="bd519-232">(Notez que, dans la mesure où les contacts de l’utilisateur ont été précédemment transférés dans le magasin de contacts unifié, les informations de contact Exchange seront utilisées).</span><span class="sxs-lookup"><span data-stu-id="bd519-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="bd519-233">Ce scénario ne nécessite aucune intervention de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bd519-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="bd519-234">**Scénario 2 :** Les contacts des utilisateurs étaient auparavant stockés dans le magasin de contacts unifié, puis restaurés.</span><span class="sxs-lookup"><span data-stu-id="bd519-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="bd519-235">Une restauration est effectuée à partir d’une sauvegarde de serveur Lync effectuée lorsque les contacts de l’utilisateur ont été stockés dans le magasin de contacts unifié.</span><span class="sxs-lookup"><span data-stu-id="bd519-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="bd519-236">Dans ce scénario, un message d’erreur `Error: Incorrect Exchange Version` figurant dans les journaux du client ou du serveur Lyss est susceptible de signaler un problème.</span><span class="sxs-lookup"><span data-stu-id="bd519-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="bd519-237">L’utilisateur sera en mesure d’accéder à sa liste de contacts dans Lync 2013 directement à partir d’Exchange, mais l’état du client ne correspond pas à l’état du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="bd519-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="bd519-238">Pour résoudre ce problème, un administrateur doit exécuter les applets de cmdlet **Invoke-CsUCSRollback** pour les utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="bd519-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="bd519-239">Les **données d’archivage** peuvent être stockées dans Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="bd519-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="bd519-240">Cette information n’est pas essentielle pour Lync Server, mais elle peut être essentielle pour les fins réglementaires de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bd519-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="bd519-241">Si les données d’archivage sont stockées dans Exchange et sont importantes pour votre organisation, suivez les procédures de sauvegarde et de restauration d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="bd519-242">Notez que les données d’archivage stockées dans Exchange ne peuvent pas être replacées sur Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bd519-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="bd519-243">Par ailleurs, il est impossible de déplacer des données déjà stockées dans la base de données d’archivage Lync vers Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd519-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="bd519-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd519-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

