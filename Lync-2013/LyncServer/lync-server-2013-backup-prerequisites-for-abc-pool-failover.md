---
title: 'Lync Server 2013 : prérequis de sauvegarde pour le basculement de pool ABC'
description: 'Lync Server 2013 : conditions préalables à la sauvegarde pour le basculement de pool ABC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup prerequisites for ABC pool failover
ms:assetid: 652046f5-6086-4592-902d-d5789581977d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945634(v=OCS.15)
ms:contentKeyID: 51541485
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 05eb0d2ad50f1ed4f04964158fb5d22d079f3b50
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437909"
---
# <a name="backup-prerequisites-for-abc-pool-failover-in-lync-server-2013"></a><span data-ttu-id="b7f12-103">Conditions préalables à la sauvegarde du basculement de pool ABC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7f12-103">Backup prerequisites for ABC pool failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7f12-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7f12-104">

<span> </span></span></span>

<span data-ttu-id="b7f12-105">_**Dernière modification de la rubrique :** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="b7f12-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="b7f12-106">Pour tirer le meilleur parti de l’utilisation de la procédure de basculement de pool ABC, vous devez effectuer certaines sauvegardes avant le désastre et le basculement.</span><span class="sxs-lookup"><span data-stu-id="b7f12-106">To get the maximum benefit from using the ABC pool failover procedure, you must perform certain backups before the disaster and failover happen:</span></span>

  - <span data-ttu-id="b7f12-107">Lorsque vous utilisez l’applet de cmdlet **Export-CsLISConfiguration** , vous devez régulièrement sauvegarder les données de configuration de l’emplacement de la base de données de la liste.</span><span class="sxs-lookup"><span data-stu-id="b7f12-107">You must regularly back up the Location Information Service (LIS) configuration data from pool A by using the **Export-CsLISConfiguration** cmdlet.</span></span>
    
        Export-csLisConfiguration -FileName <C:\LISExportPrimary.zip>

  - <span data-ttu-id="b7f12-108">Vous devez régulièrement sauvegarder les données de configuration du groupe de réponses dans le pool A à l’aide de l’applet de passe **Export-CsRgsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b7f12-108">You must regularly back up the Response Group configuration data in pool A by using the **Export-CsRgsConfiguration** cmdlet.</span></span>
    
        Export-CsRgsConfiguration -Source "service:ApplicationServer:<Pool A FQDN>" -FileName "C:\RgsExportPrimary.zip"
    
    <span data-ttu-id="b7f12-109">En règle générale, il est recommandé d’effectuer des sauvegardes journalières, mais si vous avez un volume élevé de modifications, vous souhaiterez peut-être planifier des sauvegardes plus fréquentes.</span><span class="sxs-lookup"><span data-stu-id="b7f12-109">In general, we recommend that you perform daily backups, but if you have a high volume of changes, you might want to schedule more frequent backups.</span></span> <span data-ttu-id="b7f12-110">La quantité d’informations que vous pouvez perdre en cas de sinistre dépend de la fréquence de vos sauvegardes, ainsi que de la fréquence et du volume des modifications.</span><span class="sxs-lookup"><span data-stu-id="b7f12-110">The amount of information that you can lose in the event of a disaster depends on the frequency of your backups, as well as on the frequency and volume of changes.</span></span>
    
    <span data-ttu-id="b7f12-111">L’application de groupe de réponse ne peut stocker qu’un ensemble de paramètres au niveau de l’application par liste.</span><span class="sxs-lookup"><span data-stu-id="b7f12-111">The Response Group application can store only one set of application-level settings per pool.</span></span> <span data-ttu-id="b7f12-112">Pour accéder à ces paramètres, vous pouvez utiliser les applets **de applet Get-CsRgsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b7f12-112">These settings can be accessed through the **Get-CsRgsConfiguration** cmdlets.</span></span> <span data-ttu-id="b7f12-113">Les paramètres incluent la configuration par défaut de Music-Hold en attente, le fichier audio de musique par défaut, la période de grâce à la sonnerie de l’agent et la configuration du contexte d’appel.</span><span class="sxs-lookup"><span data-stu-id="b7f12-113">The settings include the default music-on-hold configuration, the default music-on-hold audio file, the agent ring-back grace period, and the call context configuration.</span></span> <span data-ttu-id="b7f12-114">Ces paramètres peuvent être transférés d’un pool à un autre par le biais de l’applet de commande **Import-CsRgsConfiguration** à l’aide du paramètre **ReplaceExistingSettings** , mais cette opération remplacera tout paramètre au niveau de l’application dans le pool de destination.</span><span class="sxs-lookup"><span data-stu-id="b7f12-114">These settings can be transferred from one pool to another through the **Import-CsRgsConfiguration** cmdlet by using the **ReplaceExistingSettings** parameter, but this operation will override any application-level settings in the destination pool.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="b7f12-115">Dans un autre emplacement, conservez une copie de sauvegarde de tous les fichiers audio d’origine que vous avez utilisés pour configurer l’application Response Group (c’est-à-dire tout enregistrement ou fichier de musique en attente).</span><span class="sxs-lookup"><span data-stu-id="b7f12-115">In a separate location, keep a backup copy of all the original audio files that have been used to configure the Response Group application (that is, any recordings or music-on-hold files).</span></span>

    
    </div>
    
    <span data-ttu-id="b7f12-116">Si vous avez des fichiers personnalisés de musique en attente qui ont été téléchargés pour le parc d’appels dans une liste, vous devez conserver une copie de celles-ci dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="b7f12-116">If you have any customized music-on-hold files that have been uploaded for Call Park in a pool, you should keep a copy of these in another location.</span></span> <span data-ttu-id="b7f12-117">Ces fichiers ne sont pas sauvegardés dans le cadre du processus de récupération d’urgence de Lync Server 2013 et sont perdus si les fichiers téléchargés sur le pool sont endommagés, endommagés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="b7f12-117">These files are not backed up as part of the Lync Server 2013 disaster recovery process, and they will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>
    
        Xcopy  <Source: Pool A CPS File Store Path>  <Destination>
        Example: Xcopy  "<Pool A File Store Path>\LyncFileStore\coX-ApplicationServer-X\AppServerFiles\CPS\"  "<Destination:  Backup location 1>"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b7f12-118">L’application de parc d’appels ne peut stocker qu’un seul ensemble de paramètres et un fichier audio en attente personnalisé par liste.</span><span class="sxs-lookup"><span data-stu-id="b7f12-118">The Call Park application can store only one set of settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="b7f12-119">Pour accéder à ces paramètres, vous pouvez utiliser l’applet de passe <STRONG>Get-CsCpsConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="b7f12-119">These settings can be accessed through the <STRONG>Get-CsCpsConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="b7f12-120">Dans la mesure où le mécanisme de reprise après sinistre pour le stationnement d’appels repose sur l’application de parc d’appels du pool de sauvegarde, les paramètres du pool principal ne sont pas sauvegardés ou conservés en cas de sinistre.</span><span class="sxs-lookup"><span data-stu-id="b7f12-120">Because the disaster recovery mechanism for Call Park relies on the Call Park application of the backup pool, the settings of the primary pool are not backed up or preserved if a disaster occurs.</span></span> <span data-ttu-id="b7f12-121">Si le pool principal est perdu, ces paramètres ne peuvent pas être récupérés, et lorsqu’un nouveau pool est déployé pour remplacer le pool principal, les paramètres du parc d’appels et tout fichier audio de musique personnalisé doit être reconfiguré.</span><span class="sxs-lookup"><span data-stu-id="b7f12-121">If the primary pool is lost, these settings cannot be recovered, and when a new pool is deployed to replace the primary pool, the Call Park settings and any customized music-on-hold audio file would need to be reconfigured.</span></span>

    
    </div>

  - <span data-ttu-id="b7f12-122">Si vous configurez des annonces dans le cadre de la fonctionnalité de voix numérique non affectées, nous vous recommandons de conserver dans un autre emplacement une copie de tout fichier audio d’origine utilisé lors de la configuration initiale.</span><span class="sxs-lookup"><span data-stu-id="b7f12-122">If you configure any announcements as part of the Unassigned Number Voice Feature, we recommend that you keep in another location a copy of any original audio file used during the initial configuration.</span></span> <span data-ttu-id="b7f12-123">Si ce n’est pas le cas, vous pouvez obtenir une copie des fichiers audio configurés dans le magasin de fichiers du serveur ou du pool dans lequel les fichiers audio ont été importés.</span><span class="sxs-lookup"><span data-stu-id="b7f12-123">If you did not do that, you can get a copy of the configured audio files in the file store of the server or pool to which the audio files were imported.</span></span> <span data-ttu-id="b7f12-124">Ces fichiers ne sont pas sauvegardés dans le cadre du processus de récupération d’urgence de Lync Server 2013 et sont perdus si les fichiers téléchargés sur le pool sont endommagés, endommagés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="b7f12-124">These files are not backed up as part of the Lync Server 2013 disaster recovery process, and they will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="b7f12-125">Pour copier tous les fichiers audio utilisés pour configurer la fonctionnalité vocale numérique non affectée à partir du magasin de fichiers d’un serveur ou d’un pool, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b7f12-125">To copy all the audio files used to configure the Unassigned Number Voice Feature from the file store of a server or a pool, use:</span></span>
    
        Use: Xcopy  <Source: Pool A Announcement Service File Store Path>  <Destination>
        Example Usage:  Xcopy  "<Pool A File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS"  "<Destination: Backup location>"

  - <span data-ttu-id="b7f12-126">Si vous avez surveillé et archivé des bases de données dans un pool, vous devez utiliser les outils de gestion SQL Server pour les sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="b7f12-126">If you have Monitoring and Archiving databases in a pool, you should use SQL Server management tools to back them up.</span></span> <span data-ttu-id="b7f12-127">Dans la procédure de basculement ABC, les bases de données de surveillance et d’archivage ne sont pas conservées si celles-ci sont colocalisées dans le pool A, car elles ne sont pas sauvegardées via le service de sauvegarde de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b7f12-127">In the ABC failover procedure, Monitoring and Archiving databases are not preserved if they are collocated in pool A, because these databases are not backed up through Lync Server Backup Service.</span></span>

<span data-ttu-id="b7f12-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7f12-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

