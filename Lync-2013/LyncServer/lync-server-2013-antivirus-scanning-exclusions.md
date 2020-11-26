---
title: 'Lync Server 2013 : exclusions de l’analyse antivirus'
description: 'Lync Server 2013 : exclusions de l’analyse antivirus.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440660"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="984e1-103">Exclusions de l’analyse antivirus pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="984e1-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="984e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="984e1-104">

<span> </span></span></span>

<span data-ttu-id="984e1-105">_**Dernière modification de la rubrique :** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="984e1-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="984e1-106">Pour vous assurer que le scanner antivirus n’interagit pas avec le fonctionnement de Lync Server 2013, vous devez exclure les processus et répertoires spécifiques pour chaque serveur Lync Server 2013 Server ou le rôle serveur sur lequel vous exécutez un scanneur antivirus.</span><span class="sxs-lookup"><span data-stu-id="984e1-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="984e1-107">Vous devez exclure les processus et les répertoires suivants :</span><span class="sxs-lookup"><span data-stu-id="984e1-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="984e1-108">Emplacement des dossiers et fichiers indiqués ci-dessous sont les emplacements par défaut de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="984e1-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="984e1-109">Pour les emplacements pour lesquels vous n’avez pas utilisé la valeur par défaut, excluez les emplacements spécifiés pour votre organisation au lieu des emplacements par défaut spécifiés dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="984e1-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="984e1-110">Notez que certains programmes antivirus peuvent avoir besoin de chemins d’accès absolus, non relatifs, pour leur liste d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="984e1-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="984e1-111">Processus Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="984e1-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="984e1-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="984e1-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="984e1-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="984e1-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="984e1-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="984e1-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="984e1-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="984e1-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="984e1-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="984e1-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="984e1-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="984e1-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="984e1-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="984e1-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="984e1-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="984e1-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="984e1-135">Processus du service d’hôte Windows Fabric :</span><span class="sxs-lookup"><span data-stu-id="984e1-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="984e1-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="984e1-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="984e1-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-138">FabricHost.exe</span></span>

  - <span data-ttu-id="984e1-139">Processus d’IIS :</span><span class="sxs-lookup"><span data-stu-id="984e1-139">IIS processes:</span></span>
    
      - <span data-ttu-id="984e1-140">% systemroot% \\ system32 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="984e1-141">% systemroot% \\ SysWOW64 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="984e1-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="984e1-142">Processus du serveur dorsal SQL Server :</span><span class="sxs-lookup"><span data-stu-id="984e1-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="984e1-143">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. \\SQLServr.exe MSSQLSERVER MSSQL \\ Binn \\</span><span class="sxs-lookup"><span data-stu-id="984e1-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="984e1-144">% ProgramFiles% \\ Microsoft SQL Server \\ MSRS11.ReportingServicesService.exe de l’emplacement dans MSSQLSERVER \\ Reporting Services \\ ReportServer \\ \\</span><span class="sxs-lookup"><span data-stu-id="984e1-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="984e1-145">% ProgramFiles% \\ Microsoft SQL Server \\ MSAS11.MSMDSrv.exe de l’emplacement pour MSSQLSERVER \\ OLAP \\ \\</span><span class="sxs-lookup"><span data-stu-id="984e1-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="984e1-146">Processus du serveur SQL Server frontal :</span><span class="sxs-lookup"><span data-stu-id="984e1-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="984e1-147">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. \\SQLServr.exe MSSQL \\ LYNCLOCAL \\</span><span class="sxs-lookup"><span data-stu-id="984e1-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="984e1-148">% ProgramFiles% \\ Microsoft SQL Server \\ MSSQL11. \\SQLServr.exe MSSQL \\ RTCLOCAL \\</span><span class="sxs-lookup"><span data-stu-id="984e1-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="984e1-149">Répertoires et fichiers :</span><span class="sxs-lookup"><span data-stu-id="984e1-149">Directories and files:</span></span>
    
      - <span data-ttu-id="984e1-150">% systemroot% \\ system32 \\ LogFiles</span><span class="sxs-lookup"><span data-stu-id="984e1-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="984e1-151">% systemroot% \\ SysWOW64 \\ LogFiles</span><span class="sxs-lookup"><span data-stu-id="984e1-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="984e1-152">\\code global du GAC de l' \\ assembly% systemroot% Microsoft.NET \\ \_</span><span class="sxs-lookup"><span data-stu-id="984e1-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="984e1-153">% ProgramFiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="984e1-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="984e1-154">% ProgramFiles% \\ fichiers communs \\ Microsoft Lync Server 2013 \\ FileSystemWatcher</span><span class="sxs-lookup"><span data-stu-id="984e1-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="984e1-155">\\fichiers communs% ProgramFiles% \\ Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="984e1-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="984e1-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="984e1-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="984e1-157">Magasin de partage de fichiers (spécifié dans le générateur de topologies).</span><span class="sxs-lookup"><span data-stu-id="984e1-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="984e1-158">Les magasins de fichiers sont spécifiés dans le générateur de topologies.</span><span class="sxs-lookup"><span data-stu-id="984e1-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="984e1-159">Fichiers journaux et de données SQL Server, dont ceux pour la base de données principale, le magasin d’utilisateurs, le magasin d’archivage, le magasin de surveillance et le magasin d’applications.</span><span class="sxs-lookup"><span data-stu-id="984e1-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="984e1-160">Les fichiers journaux et de base de données peuvent être spécifiés dans le générateur de topologies.</span><span class="sxs-lookup"><span data-stu-id="984e1-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="984e1-161">Pour plus d’informations sur les données et les fichiers journaux pour chaque base de données, y compris les noms par défaut, voir [données SQL Server et emplacement des fichiers journaux pour Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="984e1-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="984e1-162">Les fichiers de données et les fichiers journaux de SQL Server, y compris ceux de la base de données frontale, du magasin Lync et du magasin RtcDatabase.</span><span class="sxs-lookup"><span data-stu-id="984e1-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="984e1-163">Ils sont généralement sous% Lecteur_Local% \\ CSData.</span><span class="sxs-lookup"><span data-stu-id="984e1-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="984e1-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="984e1-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

