---
title: 'Lync Server 2013 : Définition de la copie des journaux de transaction SQL Server entre la base de données miroir principale et la base de données secondaire de copie des journaux de transaction'
description: 'Lync Server 2013 : configuration de l’expédition du journal SQL Server entre le miroir principal et la base de données secondaire d’envoi du journal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database
ms:assetid: 4e8e9ce9-4301-47f2-a0c3-669afeb53295
ms:mtpsurl: https://technet.microsoft.com/library/JJ204887(v=OCS.15)
ms:contentKeyID: 48184119
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b1655721410da23d569af4df7aa656f3be69e383
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423959"
---
# <a name="setting-up-sql-server-log-shipping-between-the-primary-mirror-and-the-log-shipping-secondary-database-in-lync-server-2013"></a><span data-ttu-id="50c59-103">Définition de la copie des journaux de transaction SQL Server entre la base de données miroir principale et la base de données secondaire de copie des journaux de transaction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50c59-103">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50c59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50c59-104">

<span> </span></span></span>

<span data-ttu-id="50c59-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="50c59-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="50c59-106">Pour continuer, procédez comme suit pour l’envoi de journaux dans le cas où la base de données de chat persistante principale a basculé vers sa base de données miroir.</span><span class="sxs-lookup"><span data-stu-id="50c59-106">Perform the following steps for log shipping to continue if the primary Persistent Chat database is failed over to its mirror database.</span></span>

1.  <span data-ttu-id="50c59-107">Basculez manuellement vers le miroir sur la base de données de conversation persistante principale.</span><span class="sxs-lookup"><span data-stu-id="50c59-107">Manually fail over the primary Persistent Chat database to the mirror.</span></span> <span data-ttu-id="50c59-108">Pour ce faire, vous utilisez Lync Server Management Shell et l’applet **de passe Invoke-CsDatabaseFailover** .</span><span class="sxs-lookup"><span data-stu-id="50c59-108">This is done by using the Lync Server Management Shell and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="50c59-109">Pour plus d’informations, reportez-vous à la section « utilisation des cmdlets Lync Server Management Shell » du [déploiement de la mise en miroir SQL pour la haute disponibilité du serveur principal dans Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="50c59-109">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

2.  <span data-ttu-id="50c59-110">À l’aide de SQL Server Management Studio, connectez-vous à l’instance de miroir du serveur de chat permanent principal.</span><span class="sxs-lookup"><span data-stu-id="50c59-110">Using the SQL Server Management Studio, connect to the primary Persistent Chat Server mirror instance.</span></span>

3.  <span data-ttu-id="50c59-111">Assurez-vous que l’agent SQL Server est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="50c59-111">Be sure that the SQL Server Agent is running.</span></span>

4.  <span data-ttu-id="50c59-112">Cliquez avec le bouton droit sur la base de données mgc, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="50c59-112">Right-click the mgc database, and then click **Properties**.</span></span>

5.  <span data-ttu-id="50c59-113">Sous **Sélectionner une page**, cliquez sur **Envoi des journaux de transactions**.</span><span class="sxs-lookup"><span data-stu-id="50c59-113">Under **Select a page**, click **Transaction Log Shipping**.</span></span>

6.  <span data-ttu-id="50c59-114">Activez la case à cocher **Activer en tant que base de données primaire dans une configuration de la copie des journaux de transactions**.</span><span class="sxs-lookup"><span data-stu-id="50c59-114">Select the **Enable this as a primary database in a log shipping configuration** check box.</span></span>

7.  <span data-ttu-id="50c59-115">Sous **Sauvegardes des journaux de transactions**, cliquez sur **Paramètres de sauvegarde**.</span><span class="sxs-lookup"><span data-stu-id="50c59-115">Under **Transaction log backups**, click **Backup Settings**.</span></span>

8.  <span data-ttu-id="50c59-116">Dans la zone **Indiquer le chemin d’accès réseau au dossier de sauvegarde**, tapez le chemin d’accès réseau du partage que vous avez créé pour le dossier de sauvegarde du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="50c59-116">In the **Network path to the backup folder** box, type the network path to the share you created for the transaction log backup folder.</span></span>

9.  <span data-ttu-id="50c59-p102">Si le dossier de sauvegarde se trouve sur le serveur principal, tapez le chemin d’accès local au dossier de sauvegarde dans la zone **Si le dossier de sauvegarde se trouve sur le serveur principal, tapez un chemin d’accès local au dossier**. (Si le dossier de sauvegarde ne figure pas sur le serveur principal, vous pouvez laisser cette case à cocher vide.)</span><span class="sxs-lookup"><span data-stu-id="50c59-p102">If the backup folder is located on the primary server, type the local path to the backup folder in the **If the backup folder is located on the primary server, type a local path to the folder** box. (If the backup folder is not on the primary server, you can leave this box empty.)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="50c59-119">Si le compte de service SQL Server sur votre serveur principal s’exécute sous le compte système local, vous devez créer votre dossier de sauvegarde sur le serveur principal et spécifier un chemin local vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="50c59-119">If the SQL Server service account on your primary server runs under the local system account, you must create your backup folder on the primary server and specify a local path to that folder.</span></span>

    
    </div>

10. <span data-ttu-id="50c59-120">Configurez les paramètres **Supprimer les fichiers antérieurs à** et **Envoyer une alerte si aucune sauvegarde ne se produit en l’espace de**.</span><span class="sxs-lookup"><span data-stu-id="50c59-120">Configure the **Delete files older than** and **Alert if no backup occurs within** parameters.</span></span>

11. <span data-ttu-id="50c59-121">Examinez la planification des sauvegardes dans la zone **Planification** sous **Travail de sauvegarde**.</span><span class="sxs-lookup"><span data-stu-id="50c59-121">Look at the backup schedule listed in the **Schedule** box under **Backup job**.</span></span> <span data-ttu-id="50c59-122">Pour personnaliser le planning de votre installation, cliquez sur **Planning**, puis ajustez la planification de l’agent SQL Server, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="50c59-122">To customize the schedule for your installation, click **Schedule**, and adjust the SQL Server Agent schedule, as required.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="50c59-123">Utilisez les mêmes paramètres que ceux de la base de données primaire.</span><span class="sxs-lookup"><span data-stu-id="50c59-123">Use the same settings that you used for the primary database.</span></span>

    
    </div>

12. <span data-ttu-id="50c59-124">Sous **Compression**, sélectionnez **Utiliser le paramètre du serveur par défaut**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="50c59-124">Under **Compression**, select **Use the default server setting**, and click **OK**.</span></span>

13. <span data-ttu-id="50c59-125">Sous **Instances de serveurs et bases de données secondaires**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="50c59-125">Under **Secondary server instances and databases**, click **Add**.</span></span>

14. <span data-ttu-id="50c59-126">Cliquez sur **Connexion**, puis connectez-vous à l’instance de SQL Server que vous avez configurée en tant que serveur secondaire.</span><span class="sxs-lookup"><span data-stu-id="50c59-126">Click **Connect**, and connect to the instance of SQL Server that you have configured as your secondary server.</span></span>

15. <span data-ttu-id="50c59-127">Dans la zone **Base de données secondaire** sélectionnez la base de données **mgc** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="50c59-127">In the **Secondary Database** box, select the **mgc** database from the list.</span></span>

16. <span data-ttu-id="50c59-128">Sous l’onglet **Initialiser la base de données secondaire**, sélectionnez l’option **Non, la base de données secondaire est initialisée**.</span><span class="sxs-lookup"><span data-stu-id="50c59-128">On the **Initialize Secondary database** tab, select the option **No, the secondary database is initialized**.</span></span>

17. <span data-ttu-id="50c59-p104">Sous l’onglet **Copier les fichiers**, dans **Dossier de destination des fichiers copiés**, tapez le chemin d’accès du dossier dans lequel les sauvegardes des journaux de transactions doivent être copiées, puis cliquez sur **OK**. Ce dossier est souvent situé sur le serveur secondaire.</span><span class="sxs-lookup"><span data-stu-id="50c59-p104">On the **Copy Files** tab, in **Destination folder for copied files**, type the path of the folder into which the transaction logs backups should be copied, and click **OK**. This folder is often located on the secondary server.</span></span>

18. <span data-ttu-id="50c59-131">Ouvrez la liste déroulante **Créer un script de configuration**, puis sélectionnez **Créer un script de configuration dans une nouvelle fenêtre de requête**.</span><span class="sxs-lookup"><span data-stu-id="50c59-131">Open the **Script Configuration** drop-down list, and select **Script Configuration to New Query Window**.</span></span>

19. <span data-ttu-id="50c59-132">Dans la nouvelle fenêtre de requête, dans **Propriétés de la base de données**, cliquez sur **OK** pour commencer le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="50c59-132">In the new query window, in **Database Properties**, click **OK** to begin the configuration process.</span></span>

20. <span data-ttu-id="50c59-133">Sélectionnez et exécutez la première moitié de la requête (Voir l’étape 18) jusqu’à la ligne :-- \* \* \* \* \* \* end : script à exécuter sur le principal : \* \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="50c59-133">Select and run the first half of the query (see step 18) up to the line: -- \*\*\*\*\*\* End: Script to be run at Primary: \*\*\*\*\*\*.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="50c59-134">L’exécution manuelle de ce script est nécessaire car SQL Server Management Studio ne prend pas en charge plusieurs bases de données principales dans une configuration d’envoi du journal SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50c59-134">Manually running this script is necessary because SQL Server Management Studio does not support multiple primary databases in a SQL Server Log Shipping configuration.</span></span>

    
    </div>

21. <span data-ttu-id="50c59-135">Sélectionnez **Annuler** pour fermer le panneau de configuration de copie des journaux de transaction et établir une configuration de travail qui implémente correctement la copie des journaux de transaction pour la base de données primaire et la base de données en miroir (en cas de basculement). </span><span class="sxs-lookup"><span data-stu-id="50c59-135">Select **Cancel** to close the Log File shipping configuration panel and to establish a working setup that correctly implements the log file shipping for both the primary and mirrored database (in case of failover).</span></span>

22. <span data-ttu-id="50c59-136">Restaurez manuellement la base de données de conversation persistante principale sur le serveur principal.</span><span class="sxs-lookup"><span data-stu-id="50c59-136">Manually fail back the primary Persistent Chat database to the primary.</span></span> <span data-ttu-id="50c59-137">Pour ce faire, utilisez Lync Server Management Shell et l’applet **de passe Invoke-CsDatabaseFailover** .</span><span class="sxs-lookup"><span data-stu-id="50c59-137">This is done by using the Lync Server Management Shell, and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="50c59-138">Pour plus d’informations, reportez-vous à la section « utilisation des cmdlets Lync Server Management Shell » du [déploiement de la mise en miroir SQL pour la haute disponibilité du serveur principal dans Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="50c59-138">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="50c59-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c59-139">See Also</span></span>


[<span data-ttu-id="50c59-140">Déploiement de la mise en miroir SQL pour la haute disponibilité des serveurs principaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50c59-140">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
[<span data-ttu-id="50c59-141">Déploiement de la mise en miroir SQL pour la haute disponibilité des serveurs principaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50c59-141">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
  

<span data-ttu-id="50c59-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50c59-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

