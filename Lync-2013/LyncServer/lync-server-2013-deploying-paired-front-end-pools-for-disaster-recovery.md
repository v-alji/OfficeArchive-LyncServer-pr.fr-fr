---
title: 'Lync Server 2013 : Déploiement de pools frontaux couplés pour la récupération d’urgence'
description: 'Lync Server 2013 : déploiement de plages frontales couplées pour la récupération d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying paired Front End pools for disaster recovery
ms:assetid: 2f12467c-8b90-43e6-831b-a0b096427f17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204773(v=OCS.15)
ms:contentKeyID: 48183727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4846121f301d2bc7be1af9b58f0a0fef3f88e6d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429819"
---
# <a name="deploying-paired-front-end-pools-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="c1d1c-103">Déploiement de pools frontaux couplés pour la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c1d1c-103">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c1d1c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c1d1c-104">

<span> </span></span></span>

<span data-ttu-id="c1d1c-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="c1d1c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="c1d1c-106">Vous pouvez facilement déployer la topologie de reprise après sinistre des pools front-end couplés à l’aide du générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-106">You can easily deploy the disaster recovery topology of paired Front End pools using Topology Builder.</span></span>

<div>

## <a name="to-deploy-a-pair-of-front-end-pools"></a><span data-ttu-id="c1d1c-107">Pour déployer une paire de pools de serveurs frontaux</span><span class="sxs-lookup"><span data-stu-id="c1d1c-107">To deploy a pair of Front End pools</span></span>

1.  <span data-ttu-id="c1d1c-108">Si les pools sont nouveaux et ne sont pas encore définis, utilisez le générateur de topologie pour créer les pools.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-108">If the pools are new and not yet defined, use Topology Builder to create the pools.</span></span>

2.  <span data-ttu-id="c1d1c-109">Dans le générateur de topologie, cliquez avec le bouton droit sur l’un des deux pools, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-109">In Topology Builder, right-click one of the two pools, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="c1d1c-110">Cliquez sur **Résistance** dans le volet gauche, puis sélectionnez **Pool de stockage associé** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-110">Click **Resiliency** in the left pane, and then select **Associated Backup Pool** in the right pane.</span></span>

4.  <span data-ttu-id="c1d1c-p101">Dans la zone située en dessous de **Pool de stockage associé**, sélectionnez le pool que vous voulez jumeler à celui-ci. Seuls les pools existants qui ne sont pas déjà jumelés avec un autre pool peuvent être choisis.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-p101">In the box below **Associated Backup Pool**, select the pool that you want to pair with this pool. Only existing pools that are not already paired with another pool will be available to select from.</span></span>
    
    <span data-ttu-id="c1d1c-113">![36080581-db76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-db76-497d-bf9e-f02b39574d0e")</span><span class="sxs-lookup"><span data-stu-id="c1d1c-113">![36080581-db76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-db76-497d-bf9e-f02b39574d0e")</span></span>  

5.  <span data-ttu-id="c1d1c-114">Sélectionnez **Basculement et restauration automatiques pour Voice**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-114">Select **Automatic failover and failback for Voice**, and then click **OK**.</span></span>
    
    <span data-ttu-id="c1d1c-115">Quand vous affichez les détails de ce pool, le pool associé s’affiche dans le volet droit sous **Résistance**. </span><span class="sxs-lookup"><span data-stu-id="c1d1c-115">When you view the details about this pool, the associated pool now appears in the right pane under **Resiliency**.</span></span>

6.  <span data-ttu-id="c1d1c-116">Utilisez le générateur de topologie pour publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-116">Use Topology Builder to publish the topology.</span></span>

7.  <span data-ttu-id="c1d1c-p102">Si les deux pools n’étaient pas déjà déployés, déployez-les maintenant pour terminer la configuration. Vous pouvez ignorer les deux dernières étapes de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-p102">If the two pools were not yet deployed, deploy them now and the configuration will be complete. You can skip the final two steps in this procedure.</span></span>
    
    <span data-ttu-id="c1d1c-119">Cependant, si les pools étaient déjà déployés avant de définir la relation de paire, vous devez procéder aux deux dernières étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-119">However, if the pools were already deployed before you defined the paired relationship, you must complete the following two final steps.</span></span>

8.  <span data-ttu-id="c1d1c-120">Sur chaque serveur frontal des deux pools, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c1d1c-120">On every Front End Server in both pools, run the following:</span></span>
    ```console
    <system drive>\Program Files\Microsoft Lync Server 2013\Deployment\Bootstrapper.exe 
    ```
    <span data-ttu-id="c1d1c-121">Cela permet de configurer les autres services requis pour un fonctionnement correct du jumelage de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-121">This configures other services required for backup pairing to work correctly.</span></span>

9.  <span data-ttu-id="c1d1c-122">À partir d’une invite de commandes de Lync Server Management Shell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c1d1c-122">From a Lync Server Management Shell command prompt, run the following:</span></span>
    ```powershell
    Start-CsWindowsService -Name LYNCBACKUP
    ```
10. <span data-ttu-id="c1d1c-123">Forcez la synchronisation des données d’utilisateur et de conférence entre les deux pools, à l’aide des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="c1d1c-123">Force the user and conference data of both pools to be synchronized with each other, with the following cmdlets:</span></span>
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN>
       ```
    
    <span data-ttu-id="c1d1c-p103">La synchronisation des données peut durer un certain temps. Vous pouvez utiliser les applets de commande suivantes pour vérifier l’état. Assurez-vous que l’état de synchronisation dans les deux sens est stable.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-p103">Synchronizing the data may take some time. You can use the following cmdlets to check the status. Make sure that the status in both directions is in steady state.</span></span>
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN>
       ```

<div class="">


> [!NOTE]  
> <span data-ttu-id="c1d1c-127">L’option <STRONG>reprise automatique et retour automatique pour les appels vocaux</STRONG> et les intervalles de temps associés dans le générateur de topologie ne s’appliquent qu’aux fonctionnalités de résilience vocale introduites dans Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-127">The <STRONG>Automatic failover and failback for Voice</STRONG> option and the associated time intervals in Topology Builder apply only to the voice resiliency features that were introduced in Lync Server 2010.</span></span> <span data-ttu-id="c1d1c-128">La sélection de cette option ne signifie pas que le basculement du pool mentionné dans ce document est automatique.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-128">Selecting this option does not imply that the pool failover discussed in this document is automatic.</span></span> <span data-ttu-id="c1d1c-129">Le basculement et la restauration du pool requiert l’intervention manuelle d’un administrateur pour appeler respectivement les applets de commande de basculement et de restauration.</span><span class="sxs-lookup"><span data-stu-id="c1d1c-129">Pool failover and failback always require an administrator to manually invoke the failover and failback cmdlets, respectively.</span></span>



<span data-ttu-id="c1d1c-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c1d1c-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

