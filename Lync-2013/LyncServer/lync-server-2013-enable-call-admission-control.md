---
title: 'Lync Server 2013 : activer le contrôle d’admission des appels'
description: 'Lync Server 2013 : activer le contrôle d’admission des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable call admission control
ms:assetid: 80201105-18f7-4c02-9c71-8df5a952f6c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398642(v=OCS.15)
ms:contentKeyID: 48184650
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31bd352d407c3b14ac90a76fd6d53ccb312cab7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428943"
---
# <a name="enable-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="3e44e-103">Activer le contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e44e-103">Enable call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e44e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e44e-104">

<span> </span></span></span>

<span data-ttu-id="3e44e-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3e44e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3e44e-106">Une fois que vous avez configuré vos paramètres réseau pour le déploiement du contrôle d’admission des appels, vous devez activer le contrôle d’admission des appels afin de mettre en œuvre vos stratégies de bande passante.</span><span class="sxs-lookup"><span data-stu-id="3e44e-106">After you have configured your network settings for call admission control deployment, you must enable CAC to put your bandwidth policies into effect.</span></span>

<span data-ttu-id="3e44e-107">Pour plus d’informations, reportez-vous à la documentation Lync Server Management Shell pour les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e44e-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="3e44e-108">Get-Csnetworkconfiguration permettent</span><span class="sxs-lookup"><span data-stu-id="3e44e-108">Get-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkConfiguration)

  - [<span data-ttu-id="3e44e-109">Set-Csnetworkconfiguration permettent</span><span class="sxs-lookup"><span data-stu-id="3e44e-109">Set-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkConfiguration)

  - [<span data-ttu-id="3e44e-110">Remove-Csnetworkconfiguration permettent</span><span class="sxs-lookup"><span data-stu-id="3e44e-110">Remove-CsNetworkConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkConfiguration)

<div>

## <a name="to-enable-call-admission-control-by-using-management-shell"></a><span data-ttu-id="3e44e-111">Pour activer le contrôle d’admission des appels à l’aide de Management Shell</span><span class="sxs-lookup"><span data-stu-id="3e44e-111">To enable call admission control by using Management Shell</span></span>

1.  <span data-ttu-id="3e44e-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="3e44e-p101">Exécutez l’applet de commande Set-CsNetworkConfiguration pour activer le contrôle d’admission des appels dans votre réseau. Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="3e44e-p101">Run the Set-CsNetworkConfiguration cmdlet to enable CAC in your network. For example, run:</span></span>
    
        Set-CsNetworkConfiguration -EnableBandwidthPolicyCheck 1
    
    <span data-ttu-id="3e44e-115">Si vous souhaitez désactiver le contrôle d’admission des appels dans votre réseau, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3e44e-115">If you want to disable CAC in your network, run the following:</span></span>
    
        Set-CsNetworkConfiguration -EnableBandwidthPolicyCheck 0

</div>

<div>

## <a name="to-enable-call-admission-control-by-using-lync-server-control-panel"></a><span data-ttu-id="3e44e-116">Pour activer le contrôle d’admission des appels à l’aide du panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="3e44e-116">To enable call admission control by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="3e44e-117">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3e44e-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3e44e-118">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3e44e-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="3e44e-119">Dans la barre de navigation de gauche, cliquez sur **Configuration réseau**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-119">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="3e44e-120">Cliquez sur le bouton de navigation **Global**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-120">Click the **Global** navigation button.</span></span>

4.  <span data-ttu-id="3e44e-121">Cliquez sur **Global** dans la liste, puis sélectionnez **Afficher les détails** dans le menu **Edition**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-121">Click **Global** in the list, and then select **Show Details** on the **Edit** menu.</span></span>

5.  <span data-ttu-id="3e44e-122">Dans la page **Modifier la configuration globale**, activez la case à cocher **Activer le contrôle d’admission des appels**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-122">On the **Edit Global Settings** page, select the **Enable call admission control** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3e44e-123">Si vous souhaitez désactiver le contrôle d’admission des appels dans tout votre déploiement, désactivez cette case à cocher.</span><span class="sxs-lookup"><span data-stu-id="3e44e-123">If you want to disable call admission control throughout your deployment, clear this check box.</span></span>

    
    </div>

6.  <span data-ttu-id="3e44e-124">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="3e44e-124">Click **Commit**.</span></span>

<span data-ttu-id="3e44e-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e44e-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

