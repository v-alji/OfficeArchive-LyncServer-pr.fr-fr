---
title: 'Lync Server 2013 : restauration d’un serveur Standard Edition Server'
description: 'Lync Server 2013 : restauration d’un serveur Standard Edition Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a Standard Edition server
ms:assetid: d1845663-3138-4fd6-b3e7-337e294d40d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202190(v=OCS.15)
ms:contentKeyID: 51541519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2cd6976324492e0539c47999f78434e1a82706
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436222"
---
# <a name="restoring-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="dda33-103">Restauration d’un serveur Standard Edition Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dda33-103">Restoring a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dda33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dda33-104">

<span> </span></span></span>

<span data-ttu-id="dda33-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="dda33-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="dda33-106">Dans le cas contraire, suivez les procédures décrites dans cette section pour un serveur Standard Edition n’hébergeant pas le magasin central de gestion.</span><span class="sxs-lookup"><span data-stu-id="dda33-106">If a Standard Edition server that does not host the Central Management store fails, follow the procedures in this section.</span></span> <span data-ttu-id="dda33-107">Si la Banque centrale de gestion échoue, voir [restauration du serveur qui héberge le magasin de gestion central dans Lync server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span><span class="sxs-lookup"><span data-stu-id="dda33-107">If the Central Management store fails, see [Restoring the server hosting the Central Management store in Lync Server 2013](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md).</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="dda33-108">Nous vous recommandons de prendre une copie d’image du système avant de commencer la restauration.</span><span class="sxs-lookup"><span data-stu-id="dda33-108">We recommend that you take an image copy of the system before you start restoration.</span></span> <span data-ttu-id="dda33-109">Vous pouvez utiliser cette image comme point de restauration en cas de problème de restauration.</span><span class="sxs-lookup"><span data-stu-id="dda33-109">You can use this image as a rollback point, in case something goes wrong during restoration.</span></span> <span data-ttu-id="dda33-110">Vous souhaiterez peut-être prendre la copie d’image après l’installation du système d’exploitation et de SQL Server, puis restaurez ou Réinscrivez les certificats.</span><span class="sxs-lookup"><span data-stu-id="dda33-110">You might want to take the image copy after you install the operating system and SQL Server, and restore or re-enroll the certificates.</span></span>



</div>

<div>

## <a name="to-restore-a-standard-edition-server"></a><span data-ttu-id="dda33-111">Pour restaurer un serveur Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="dda33-111">To restore a Standard Edition server</span></span>

1.  <span data-ttu-id="dda33-112">Commencez par un serveur propre ou nouveau qui porte le même nom de domaine complet (FQDN) que l’ordinateur en panne, installez le système d’exploitation, puis restaurez ou Réinscrivez les certificats.</span><span class="sxs-lookup"><span data-stu-id="dda33-112">Start with a clean or new server that has the same fully qualified domain name (FQDN) as the failed computer, install the operating system, and then restore or reenroll the certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dda33-113">Pour effectuer cette étape, suivez les procédures de déploiement du serveur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dda33-113">Follow your organization's server deployment procedures to perform this step.</span></span>

    
    </div>

2.  <span data-ttu-id="dda33-114">À partir d’un compte d’utilisateur membre du groupe RTCUniversalServerAdmins et du groupe administrateurs locaux, connectez-vous au serveur que vous restaurez.</span><span class="sxs-lookup"><span data-stu-id="dda33-114">From a user account that is a member of the RTCUniversalServerAdmins group and the Local Administrators group, log on to the server that you are restoring.</span></span>

3.  <span data-ttu-id="dda33-115">Restaurez le magasin de fichiers en copiant le magasin de fichiers approprié de $Backup à l’emplacement de stockage des fichiers sur le serveur et partagez le dossier.</span><span class="sxs-lookup"><span data-stu-id="dda33-115">Restore the File Store by copying the appropriate File Store from $Backup to the File Store location on the server and share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="dda33-116">Le chemin d’accès et le nom de fichier du magasin de fichiers restauré doivent être identiques à ceux du magasin de fichiers sauvegardé pour que les composants qui les utilisent puissent y accéder.</span><span class="sxs-lookup"><span data-stu-id="dda33-116">The path and file name for the restored File Store should be exactly the same as the backed up File Store so that components that use the files can access them.</span></span>

    
    </div>

4.  <span data-ttu-id="dda33-117">Exécuter le générateur de topologie :</span><span class="sxs-lookup"><span data-stu-id="dda33-117">Run Topology Builder:</span></span>
    
    1.  <span data-ttu-id="dda33-118">Démarrer le générateur de topologie : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Générateur de topologie de Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="dda33-118">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>
    
    2.  <span data-ttu-id="dda33-119">Cliquez sur **Télécharger la topologie à partir du déploiement existant**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dda33-119">Click **Download Topology from existing deployment**, and then click **OK**.</span></span>
    
    3.  <span data-ttu-id="dda33-120">Sélectionnez la topologie, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dda33-120">Select the topology, and then click **Save**.</span></span> <span data-ttu-id="dda33-121">Cliquez sur **Oui** pour confirmer votre sélection.</span><span class="sxs-lookup"><span data-stu-id="dda33-121">Click **Yes** to confirm your selection.</span></span>

5.  <span data-ttu-id="dda33-122">Recherchez le dossier d’installation ou le média de Lync Server, puis démarrez l’Assistant Déploiement de Lync Server situé au niveau de \\ configuration de \\ \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="dda33-122">Browse to the Lync Server installation folder or media, and then start the Lync Server Deployment Wizard located at \\setup\\amd64\\Setup.exe.</span></span> <span data-ttu-id="dda33-123">Utilisez l’Assistant Déploiement de Lync Server pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dda33-123">Use the Lync Server Deployment Wizard to do the following:</span></span>
    
    1.  <span data-ttu-id="dda33-124">Exécutez l' **étape 1 : installer le magasin de configuration local** pour installer les fichiers de configuration locaux.</span><span class="sxs-lookup"><span data-stu-id="dda33-124">Run **Step 1: Install Local Configuration Store** to install the local configuration files.</span></span>
    
    2.  <span data-ttu-id="dda33-125">Exécutez l' **étape 2 : configurer ou supprimer les composants serveur Lync** pour installer les rôles serveur de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dda33-125">Run **Step 2: Setup or Remove Lync Server Components** to install the Lync Server server roles.</span></span>
    
    3.  <span data-ttu-id="dda33-126">Exécutez l' **étape 3 : demandez, installez ou attribuez des certificats** pour attribuer les certificats.</span><span class="sxs-lookup"><span data-stu-id="dda33-126">Run **Step 3: Request, Install or Assign Certificates** to assign the certificates.</span></span>
    
    4.  <span data-ttu-id="dda33-127">Exécutez l' **étape 4 : démarrer des services** pour démarrer des services sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dda33-127">Run **Step 4: Start Services** to start services on the server.</span></span>
    
    <span data-ttu-id="dda33-128">Pour plus d’informations sur l’exécution de l’Assistant Déploiement, voir la documentation de déploiement pour le rôle de serveur que vous restaurez.</span><span class="sxs-lookup"><span data-stu-id="dda33-128">For details about running the Deployment Wizard, see the Deployment documentation for the server role you are restoring.</span></span>

6.  <span data-ttu-id="dda33-129">Restaurez les données utilisateur en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="dda33-129">Restore user data by performing the following:</span></span>
    
    1.  <span data-ttu-id="dda33-130">Copiez ExportedUserData.zip de $Backup \\ dans un répertoire local.</span><span class="sxs-lookup"><span data-stu-id="dda33-130">Copy ExportedUserData.zip from $Backup\\ to a local directory.</span></span>
    
    2.  <span data-ttu-id="dda33-131">Avant de restaurer les données utilisateur, vous devez arrêter les services Lync.</span><span class="sxs-lookup"><span data-stu-id="dda33-131">Before you restore the user data, you must stop Lync services.</span></span> <span data-ttu-id="dda33-132">Pour ce faire, tapez :</span><span class="sxs-lookup"><span data-stu-id="dda33-132">To do so, type:</span></span>
        
            Stop-CsWindowsService
    
    3.  <span data-ttu-id="dda33-133">Pour restaurer les données utilisateur, à partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="dda33-133">To restore the user data, at the command line, type:</span></span>
        
            Import-CsUserData -PoolFqdn <Fqdn> -FileName <String>
        
        <span data-ttu-id="dda33-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dda33-134">For example:</span></span>
        
            Import-CsUserData -PoolFqdn "atl0cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserDatal.zip"
    
    4.  <span data-ttu-id="dda33-135">Redémarrez les services Lync en entrant :</span><span class="sxs-lookup"><span data-stu-id="dda33-135">Restart Lync services by typing:</span></span>
        
            Start-CsWindowsService

7.  <span data-ttu-id="dda33-136">Si vous avez déployé Response Group sur ce serveur Standard Edition Server, restaurez les données de configuration du groupe de réponse.</span><span class="sxs-lookup"><span data-stu-id="dda33-136">If you deployed Response Group on this Standard Edition server, restore the Response Group configuration data.</span></span> <span data-ttu-id="dda33-137">Pour plus d’informations, consultez la rubrique [restauration des paramètres du groupe de réponses dans Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span><span class="sxs-lookup"><span data-stu-id="dda33-137">For details, see [Restoring Response Group settings in Lync Server 2013](lync-server-2013-restoring-response-group-settings.md).</span></span>

8.  <span data-ttu-id="dda33-138">Si vous avez déployé une conversation persistante sur ce serveur Standard Edition Server, restaurez la base de données de chat permanent (MGC. mdf).</span><span class="sxs-lookup"><span data-stu-id="dda33-138">If you deployed Persistent Chat on this Standard Edition server, restore the Persistent Chat database (mgc.mdf).</span></span>
    
    <span data-ttu-id="dda33-139">Si vous avez utilisé la sauvegarde SQL Server pour sauvegarder la base de données de chat persistante, utilisez les procédures de restauration SQL Server pour la restaurer.</span><span class="sxs-lookup"><span data-stu-id="dda33-139">If you used SQL Server Backup to back up the Persistent Chat database, use SQL Server restore procedures to restore it.</span></span>
    
    <span data-ttu-id="dda33-140">Si vous avez utilisé le cmdlet Export-CsPersistentChatData pour le sauvegarder, utilisez la Import-CsPersistentChatData pour le restaurer.</span><span class="sxs-lookup"><span data-stu-id="dda33-140">If you used the Export-CsPersistentChatData cmdlet to back it up, use the Import-CsPersistentChatData to restore it.</span></span>

<span data-ttu-id="dda33-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dda33-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

