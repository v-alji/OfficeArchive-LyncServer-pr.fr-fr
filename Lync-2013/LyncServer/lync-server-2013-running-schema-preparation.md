---
title: 'Lync Server 2013 : Exécution de la préparation du schéma'
description: 'Lync Server 2013 : exécution d’une préparation de schéma.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running schema preparation
ms:assetid: 9d02bdb1-ff29-417a-bcce-b068b31207d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412729(v=OCS.15)
ms:contentKeyID: 48184911
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0991bbff7f54f8b8b9eb01fc87f752e00f3dcbfd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442193"
---
# <a name="running-active-directory-schema-preparation-in-lync-server-2013"></a><span data-ttu-id="7fbbf-103">Exécution de la préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fbbf-103">Running Active Directory schema preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7fbbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7fbbf-104">

<span> </span></span></span>

<span data-ttu-id="7fbbf-105">_**Dernière modification de la rubrique :** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="7fbbf-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="7fbbf-106">Vous pouvez utiliser le programme d’installation ou les applets de contrôle Lync Server Management Shell pour préparer le schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the Active Directory schema.</span></span> <span data-ttu-id="7fbbf-107">L’applet de contrôle qui étend le schéma Active Directory est **install-CsAdServerSchema**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-107">The cmdlet that extends the Active Directory schema is **Install-CsAdServerSchema**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7fbbf-108">L’applet de commande de préparation du schéma (<STRONG>install-CsAdServerSchema</STRONG>) doit accéder au maître de schéma, qui nécessite que le service Registre distant soit en cours d’exécution et que la clé de Registre à distance soit activée.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-108">The schema preparation cmdlet (<STRONG>Install-CsAdServerSchema</STRONG>) must access the schema master, which requires that the remote registry service is running and that the remote registry key is enabled.</span></span> <span data-ttu-id="7fbbf-109">Si le service Registre distant ne peut pas être activé sur le maître de schéma, vous pouvez exécuter l’applet de commande localement sur le maître de schéma.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-109">If the remote registry service cannot be enabled on the schema master, you can run the cmdlet locally on the schema master.</span></span> <span data-ttu-id="7fbbf-110">Pour plus d’informations sur l’accès à distance du Registre, voir l’article de la base de connaissances Microsoft 314837, « comment gérer l’accès distant au Registre » <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A> .</span><span class="sxs-lookup"><span data-stu-id="7fbbf-110">For details about registry remote access, see Microsoft Knowledge Base article 314837, "How to Manage Remote Access to the Registry," at <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A>.</span></span>



</div>

<span data-ttu-id="7fbbf-111">Après avoir terminé la préparation du schéma, vérifiez manuellement que la partition de schéma a été répliquée avant de procéder à la préparation de la forêt.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-111">After you complete schema preparation, manually verify that the schema partition has been replicated before proceeding to forest preparation.</span></span> <span data-ttu-id="7fbbf-112">Pour plus d’informations, consultez [vérification de la réplication de schéma Active Directory dans Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="7fbbf-112">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="7fbbf-113">Pour utiliser le programme d’installation pour préparer le schéma de la forêt actuelle</span><span class="sxs-lookup"><span data-stu-id="7fbbf-113">To use Setup to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="7fbbf-114">Ouvrez une session sur un serveur de votre forêt en tant que membre du groupe administrateurs de schéma et avec des droits d’administrateur sur le maître de schéma.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-114">Log on to a server in your forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="7fbbf-115">Dans le dossier d’installation ou le média de Lync Server 2013, exécutez Setup.exe pour démarrer l’Assistant déploiement.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-115">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="7fbbf-116">Si vous êtes invité à installer le package redistribuable Microsoft Visual C++, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-116">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>

4.  <span data-ttu-id="7fbbf-117">La boîte de dialogue de configuration de Lync Server 2013 vous invite à entrer un emplacement d’installation des fichiers du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-117">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="7fbbf-118">Choisissez l’emplacement par défaut ou **Naviguez** jusqu’à l’emplacement de votre choix, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-118">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>

5.  <span data-ttu-id="7fbbf-119">Sur la page contrat de licence, activez la case à cocher **J’accepte les termes du contrat de licence**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-119">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span>

6.  <span data-ttu-id="7fbbf-120">Le programme d’installation installe les composants principaux de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-120">The installer installs the Lync Server Core Components.</span></span>

7.  <span data-ttu-id="7fbbf-121">Lorsque l’Assistant déploiement est prêt, cliquez sur **Préparer Active Directory** et attendez que l’état du déploiement soit déterminé.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-121">When the Deployment Wizard is ready, click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

8.  <span data-ttu-id="7fbbf-122">À l' **étape 1 : préparer le schéma**, cliquez sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-122">At **Step 1: Prepare Schema**, click **Run**.</span></span>

9.  <span data-ttu-id="7fbbf-123">Sur la page **préparer le schéma** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-123">On the **Prepare Schema** page, click **Next**.</span></span>

10. <span data-ttu-id="7fbbf-124">Dans la page **Exécution de commandes**, recherchez **Statut de la tâche : Terminée**, puis cliquez sur **Afficher le journal**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-124">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

11. <span data-ttu-id="7fbbf-125">Sous la colonne **action** , développez **PREP du schéma**, recherchez le résultat de l' **\<Success\>** exécution à la fin de chaque tâche pour vérifier que la préparation du schéma s’est déroulée correctement, fermez le journal, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-125">Under the **Action** column, expand **Schema Prep**, look for the **\<Success\>** Execution Result at the end of each task to verify that schema preparation completed successfully, close the log, and then click **Finish**.</span></span>

12. <span data-ttu-id="7fbbf-126">Attendez la fin de la réplication Active Directory pour qu’elle soit terminée ou forcée.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-126">Wait for Active Directory replication to complete or force replication.</span></span>

13. <span data-ttu-id="7fbbf-127">Assurez-vous manuellement que les modifications du schéma sont répliquées sur tous les autres contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-127">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="7fbbf-128">Pour plus d’informations, consultez [vérification de la réplication de schéma Active Directory dans Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="7fbbf-128">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="7fbbf-129">Pour utiliser des applets de cmdlet pour préparer le schéma de la forêt actuelle</span><span class="sxs-lookup"><span data-stu-id="7fbbf-129">To use cmdlets to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="7fbbf-130">Ouvrez une session sur un ordinateur de la forêt en tant que membre du groupe administrateurs de schéma et avec des droits d’administrateur sur le maître de schéma.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-130">Log on to a computer in the forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="7fbbf-131">Installez les composants principaux de Lync Server comme suit :</span><span class="sxs-lookup"><span data-stu-id="7fbbf-131">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="7fbbf-132">Dans le dossier d’installation ou le média de Lync Server 2013, exécutez Setup.exe pour démarrer l’Assistant Déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-132">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="7fbbf-133">Si vous êtes invité à installer le package redistribuable Microsoft Visual C++, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-133">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="7fbbf-134">La boîte de dialogue de configuration de Lync Server 2013 vous invite à entrer un emplacement d’installation des fichiers du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-134">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="7fbbf-135">Choisissez l’emplacement par défaut ou **Naviguez** jusqu’à l’emplacement de votre choix, puis cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-135">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="7fbbf-136">Sur la page contrat de licence, activez la case à cocher **J’accepte les termes du contrat de licence**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-136">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="7fbbf-137">Le programme d’installation installe les composants principaux de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-137">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="7fbbf-138">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="7fbbf-139">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="7fbbf-139">Run:</span></span>
    
        Install-CsAdServerSchema [-Ldf <directory where the .ldf file is located>] 
    
    <span data-ttu-id="7fbbf-140">Si vous ne spécifiez pas le paramètre LDF, la valeur par défaut correspond au chemin d’accès de l’installation de Lync Server 2013 lu à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-140">If you do not specify the Ldf parameter, the default value is the Lync Server 2013 installation path that is read from the registry.</span></span>
    
    <span data-ttu-id="7fbbf-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7fbbf-141">For example:</span></span>
    
        Install-CsAdServerSchema -Ldf "C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup"

5.  <span data-ttu-id="7fbbf-142">Utilisez l’applet de commande suivante pour vérifier que la préparation du schéma s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-142">Use the following cmdlet to verify that schema preparation ran to completion.</span></span>
    
        Get-CsAdServerSchema 
    
    <span data-ttu-id="7fbbf-143">Cette applet de contrôle renvoie une valeur de l' **État de version du schéma \_ \_ \_ en cours** si la préparation du schéma a réussi.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-143">This cmdlet returns a value of **SCHEMA\_VERSION\_STATE\_CURRENT** if schema preparation was successful.</span></span>

6.  <span data-ttu-id="7fbbf-144">Attendez la fin de la réplication Active Directory pour qu’elle soit terminée ou forcée.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-144">Wait for Active Directory replication to complete or force replication.</span></span>

7.  <span data-ttu-id="7fbbf-145">Assurez-vous manuellement que les modifications du schéma sont répliquées sur tous les autres contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="7fbbf-145">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="7fbbf-146">Pour plus d’informations, consultez [vérification de la réplication de schéma Active Directory dans Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="7fbbf-146">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7fbbf-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fbbf-147">See Also</span></span>


[<span data-ttu-id="7fbbf-148">Vérification de la réplication de schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fbbf-148">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)  


[<span data-ttu-id="7fbbf-149">Préparation du schéma Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fbbf-149">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="7fbbf-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7fbbf-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

