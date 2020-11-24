---
title: Supprimer l’association au serveur d’archivage
description: Supprimez l’Association du serveur d’archivage.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Archiving server association
ms:assetid: dabac157-71ee-4afe-b0b6-4a083d165ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721903(v=OCS.15)
ms:contentKeyID: 49733837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f6c34e49b0217a8318a83752b3878a7625e5d58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395249"
---
# <a name="remove-the-archiving-server-association"></a><span data-ttu-id="ceb43-103">Supprimer l’association au serveur d’archivage</span><span class="sxs-lookup"><span data-stu-id="ceb43-103">Remove the Archiving server association</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ceb43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ceb43-104">

<span> </span></span></span>

<span data-ttu-id="ceb43-105">_**Dernière modification de la rubrique :** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="ceb43-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="ceb43-106">Pour supprimer un serveur d’archivage, vous devez modifier ou effacer la dépendance sur le pool frontal associé, le serveur frontal, l’unité de branchement Survivable et le serveur de succursales survivant.</span><span class="sxs-lookup"><span data-stu-id="ceb43-106">To remove an Archiving Server, you need to change or clear the dependency on the associated Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server.</span></span> <span data-ttu-id="ceb43-107">Vous pouvez modifier les propriétés du pool frontal, du serveur frontal, de l’unité de branchement Survivable et du serveur de succursales survivant pour supprimer la dépendance.</span><span class="sxs-lookup"><span data-stu-id="ceb43-107">You edit the properties of the Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server to remove the dependency.</span></span> <span data-ttu-id="ceb43-108">Une fois que vous avez effacé les dépendances et que vous avez supprimé le serveur dans le générateur de topologie, vous êtes informé que l’objet du magasin de base de données associé dans le générateur de topologie sera également supprimé.</span><span class="sxs-lookup"><span data-stu-id="ceb43-108">After you clear the dependency and you delete the server in Topology Builder, you are notified that the associated database store object in Topology Builder will also be deleted.</span></span>

<div>

## <a name="to-remove-the-archiving-server-association"></a><span data-ttu-id="ceb43-109">Pour supprimer l’Association du serveur d’archivage</span><span class="sxs-lookup"><span data-stu-id="ceb43-109">To remove the Archiving Server association</span></span>

1.  <span data-ttu-id="ceb43-110">Ouvrez le serveur frontal Lync Server 2013, ouvrez le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="ceb43-110">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="ceb43-111">Accédez au nœud Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="ceb43-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="ceb43-112">Dans le générateur de topologie, développez **Pools front end Edition**, **serveurs front end Standard Edition** ou **sites de succursales** en fonction de l’emplacement de définition du serveur d’archivage.</span><span class="sxs-lookup"><span data-stu-id="ceb43-112">In Topology Builder, expand **Enterprise Edition Front End pools**, **Standard Edition Front End Servers**, or **Branch sites**, based on where the Archiving Server is defined.</span></span>

4.  <span data-ttu-id="ceb43-113">Si vous avez un serveur de succursales Survivable associé, développez **sites de succursales**, développez le nom du site de la succursale, puis développez **appareils de branchement survivables**.</span><span class="sxs-lookup"><span data-stu-id="ceb43-113">If you have Survivable Branch Server associated, expand **Branch sites**, expand the branch site name, and then expand **Survivable Branch Appliances**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ceb43-114">Les <STRONG>appareils de branchement survivables</STRONG> dans l’interface utilisateur s’appliquent à la fois au serveur de succursales survivant et au dispositif de branchement survivant.</span><span class="sxs-lookup"><span data-stu-id="ceb43-114"><STRONG>Survivable Branch Appliances</STRONG> in the user interface applies to both Survivable Branch Server and Survivable Branch Appliance.</span></span>

    
    </div>

5.  <span data-ttu-id="ceb43-115">Cliquez avec le bouton droit sur le pool, le serveur ou l’appareil associé au serveur d’archivage, puis cliquez sur **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ceb43-115">Right-click the pool, server, or device that is associated with the Archiving Server, and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="ceb43-116">Dans la boîte de **dialogue Modifier les propriétés**, sous **général**, sous **associations**, décochez la case associer un **serveur d’archivage** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ceb43-116">In **Edit Properties**, under **General**, under **Associations**, clear the **Associate Archiving Server** check box, and then click **OK**.</span></span>

7.  <span data-ttu-id="ceb43-117">Répétez l’étape précédente pour tout autre serveur ou appareil associé au serveur d’archivage que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="ceb43-117">Repeat the previous step for any other pool, server or device associated with the Archiving Server that you want to remove.</span></span>

8.  <span data-ttu-id="ceb43-118">Cliquez avec le bouton droit sur le serveur d’archivage, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="ceb43-118">Right-click the Archiving Server, and then click **Delete**.</span></span>

9.  <span data-ttu-id="ceb43-119">Sur **Supprimer les magasins dépendants**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ceb43-119">On **Delete Dependent Stores**, click **OK**.</span></span>

10. <span data-ttu-id="ceb43-120">Publiez la topologie, vérifiez l’état de la réplication, puis exécutez l’Assistant Déploiement de Lync Server selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ceb43-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="ceb43-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ceb43-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

