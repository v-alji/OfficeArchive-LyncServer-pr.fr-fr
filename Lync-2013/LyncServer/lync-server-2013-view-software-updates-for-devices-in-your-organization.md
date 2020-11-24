---
title: 'Lync Server 2013 : afficher les mises à jour logicielles pour les appareils de votre organisation'
description: 'Lync Server 2013 : afficher les mises à jour logicielles des appareils de votre organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View software updates for devices in your organization
ms:assetid: d2cca12b-ed43-4e1f-90ab-d14bca8b482c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182592(v=OCS.15)
ms:contentKeyID: 48185418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 833ab25315847b760271c63bbfca3ba8357e41c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394668"
---
# <a name="view-software-updates-for-devices-in-lync-server-2013"></a><span data-ttu-id="e2034-103">Afficher les mises à jour logicielles des appareils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2034-103">View software updates for devices in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2034-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2034-104">

<span> </span></span></span>

<span data-ttu-id="e2034-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e2034-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e2034-106">Avec Lync Server 2013, vous utilisez le service Web de mise à jour des périphériques pour afficher et gérer les mises à jour logicielles des appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e2034-106">With Lync Server 2013, you use Device Update Web service to view and manage software updates for your organization’s devices.</span></span> <span data-ttu-id="e2034-107">Ces mises à jour sont disponibles dans des fichiers. cab (CAB) sur le site Web du support Microsoft à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) .</span><span class="sxs-lookup"><span data-stu-id="e2034-107">These updates are available in .cab (cabinet) files from the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091).</span></span> <span data-ttu-id="e2034-108">Après avoir téléchargé le fichier. cab, exécutez l’applet de passe **Import-CSDeviceUpdate** pour importer les règles de mise à jour de l’appareil à partir du fichier. cab.</span><span class="sxs-lookup"><span data-stu-id="e2034-108">After you download the .cab file, run the **Import-CSDeviceUpdate** cmdlet to import the device update rules from the .cab file.</span></span> <span data-ttu-id="e2034-109">Pour plus d’informations sur l’applet de connexion **Import-CSDeviceUpdate** , voir [Import-CSDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) dans la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="e2034-109">For details about the **Import-CSDeviceUpdate** cmdlet, see [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) in the Lync Server Management Shell documentation.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="e2034-110">Avant de déployer une nouvelle mise à jour de votre organisation, vérifiez qu’elle fonctionne correctement sur un appareil de test.</span><span class="sxs-lookup"><span data-stu-id="e2034-110">Before deploying a new update to your organization, verify that it functions correctly on a test device.</span></span>



</div>

<div>

## <a name="to-view-software-updates-for-uc-devices"></a><span data-ttu-id="e2034-111">Pour afficher les mises à jour logicielles des appareils UC</span><span class="sxs-lookup"><span data-stu-id="e2034-111">To view software updates for UC devices</span></span>

1.  <span data-ttu-id="e2034-112">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="e2034-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e2034-113">Sur le site Web du support Microsoft à [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091) , téléchargez le fichier. cab vers un emplacement sur un ordinateur Lync Server 2013 (par exemple, C : \\ mises à jour \\UCUpdates.cab).</span><span class="sxs-lookup"><span data-stu-id="e2034-113">From the Microsoft Support website at [https://go.microsoft.com/fwlink/p/?linkId=204091](https://go.microsoft.com/fwlink/p/?linkid=204091), download the .cab file to a location on a Lync Server 2013 computer (for example, C:\\Updates\\UCUpdates.cab).</span></span>

3.  <span data-ttu-id="e2034-114">Importez les règles de mise à jour de l’appareil à partir du C : \\ mises à jour \\UCUpdates.cab fichier en exécutant l’une des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2034-114">Import the device update rules from the C:\\Updates\\UCUpdates.cab file by running one of the following cmdlets:</span></span>
    
      - <span data-ttu-id="e2034-115">Si le fichier. cab se trouve sur le même ordinateur que celui exécutant le service à mettre à jour (service : Redmond-WebSvc-2), exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e2034-115">If the .cab file is located on the same computer as the one running the service to be updated (service:Redmond-websvc-2), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-2 -FileName C:\Updates\UCUpdates.cab
    
      - <span data-ttu-id="e2034-116">Si le fichier. cab se trouve sur un ordinateur autre que celui exécutant le service à mettre à jour (service : Redmond-WebSvc-3), exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="e2034-116">If the .cab file is located on a different computer than the one running the service to be updated (service:Redmond-websvc-3), run the following cmdlet:</span></span>
        
            Import-CsDeviceUpdate -Identity service:Redmond-websvc-3 -ByteInput C:\Updates\UCUpdates.cab

4.  <span data-ttu-id="e2034-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2034-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e2034-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e2034-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

5.  <span data-ttu-id="e2034-119">Dans la barre de navigation gauche, cliquez sur **clients**, puis cliquez sur **mise à jour** de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2034-119">In the left navigation bar, click **Clients**, and then click **Device Update**.</span></span>

6.  <span data-ttu-id="e2034-120">Dans la page **mise à jour** de l’appareil, cliquez sur une mise à jour dans la liste, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2034-120">On the **Device Update** page, click an update in the list, and then do one of the following:</span></span>
    
      - <span data-ttu-id="e2034-121">**Annuler une mise à jour en attente.**</span><span class="sxs-lookup"><span data-stu-id="e2034-121">**Cancel a pending update.**</span></span> <span data-ttu-id="e2034-122">Pour empêcher le déploiement de la mise à jour sélectionnée sur les appareils de votre organisation, cliquez sur le menu **action** , puis cliquez sur **annuler les mises à jour en attente**.</span><span class="sxs-lookup"><span data-stu-id="e2034-122">To prevent the selected update from being deployed to your organization’s devices, click the **Action** menu, and then click **Cancel pending updates**.</span></span>
    
      - <span data-ttu-id="e2034-123">**Approuver une mise à jour.**</span><span class="sxs-lookup"><span data-stu-id="e2034-123">**Approve an update.**</span></span> <span data-ttu-id="e2034-124">Pour autoriser le déploiement de la mise à jour sélectionnée sur les appareils de votre organisation, cliquez sur le menu **action** , puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="e2034-124">To allow the selected update to be deployed to your organization’s devices, click the **Action** menu, and then click **Approve**.</span></span>
    
      - <span data-ttu-id="e2034-125">**Restaurer une mise à jour.**</span><span class="sxs-lookup"><span data-stu-id="e2034-125">**Restore an update.**</span></span> <span data-ttu-id="e2034-126">Pour autoriser la mise à jour des mises à jour précédemment approuvées sur les appareils de votre organisation, cliquez sur le menu **action** , puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="e2034-126">To allow a previously approved update to be deployed to your organization’s devices, click the **Action** menu, and then click **Restore**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e2034-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2034-127">See Also</span></span>


[<span data-ttu-id="e2034-128">Gestion des appareils, des téléphones et des applications client dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2034-128">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="e2034-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2034-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

