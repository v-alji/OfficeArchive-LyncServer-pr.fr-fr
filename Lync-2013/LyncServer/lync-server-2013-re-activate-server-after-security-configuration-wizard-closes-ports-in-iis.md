---
title: Réactivation du serveur après la fermeture des ports par l’Assistant Configuration de la sécurité dans les services Internet (IIS)
description: Réactivez serveur après que l’Assistant Configuration de la sécurité ferme les ports dans IIS.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436719"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a><span data-ttu-id="856b5-103">Réactivation du serveur après la fermeture des ports par l’Assistant Configuration de la sécurité dans les services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="856b5-103">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="856b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="856b5-104">

<span> </span></span></span>

<span data-ttu-id="856b5-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="856b5-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="856b5-106">Certains rôles Lync Server 2013 exécutent des services Web sur Internet Information Services (IIS) 4443.</span><span class="sxs-lookup"><span data-stu-id="856b5-106">Some Lync Server 2013 roles run Web Services on Internet Information Services (IIS) port 4443.</span></span> <span data-ttu-id="856b5-107">En exécutant l’Assistant Déploiement de Lync Server, Bootstrapper.exe ou en utilisant l’applet de action **Enable-CsComputer** , vous créez une exception dans le pare-feu et ouvrez le port.</span><span class="sxs-lookup"><span data-stu-id="856b5-107">Running the Lync Server Deployment Wizard, Bootstrapper.exe, or using the **Enable-CsComputer** cmdlet creates an exception in the firewall and opens the port.</span></span> <span data-ttu-id="856b5-108">Si vous exécutez ensuite l’Assistant Configuration de la sécurité Windows Server 2008 R2 (ou d’autres scripts de renforcement), le port 4443 sera bloqué et les clients externes ne seront pas en mesure de contacter les services Web.</span><span class="sxs-lookup"><span data-stu-id="856b5-108">If you then run the Windows Server 2008 R2 Security Configuration Wizard (or other hardening scripts), port 4443 will be blocked, and external clients will not be able to contact Web Services.</span></span> <span data-ttu-id="856b5-109">Pour rouvrir le port, vous pouvez modifier directement l’exception de pare-feu ou réactiver le serveur.</span><span class="sxs-lookup"><span data-stu-id="856b5-109">To reopen the port you can either modify the firewall exception directly or re-activate the server.</span></span>

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a><span data-ttu-id="856b5-110">Pour réactiver le serveur à l’aide de l’Assistant Déploiement</span><span class="sxs-lookup"><span data-stu-id="856b5-110">To re-activate the server by using the Deployment Wizard</span></span>

1.  <span data-ttu-id="856b5-111">Dans la page Assistant Déploiement de Lync Server, cliquez sur **exécuter** à côté de l' **étape 2 : configurer ou supprimer les composants Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="856b5-111">On the Lync Server Deployment Wizard page, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

2.  <span data-ttu-id="856b5-112">Sur la page **Configuration des composants du serveur Lync** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="856b5-112">On **Setup Lync Server components** page, click **Next**.</span></span>

3.  <span data-ttu-id="856b5-113">Dans la page **exécution des commandes** , lorsque l’état de la tâche est affiché comme terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="856b5-113">On the **Executing Commands** page, when the task status is shown as completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="856b5-114">Vous pouvez également utiliser bootstrapper.exe ou <STRONG>Enable-CsComputer</STRONG> pour réactiver le serveur.</span><span class="sxs-lookup"><span data-stu-id="856b5-114">You can also use bootstrapper.exe or <STRONG>Enable-CsComputer</STRONG> to re-activate the server.</span></span>

    
    <span data-ttu-id="856b5-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="856b5-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

