---
title: Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server sur un site de succursale - tâche de site de succursale
description: Déploiement d’une tâche de succursale ou d’un serveur de succursales survivant.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy a Survivable Branch Appliance or Server - branch site task
ms:assetid: 7989ba29-0419-46dd-892c-4ad3238afd56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398599(v=OCS.15)
ms:contentKeyID: 48184586
ms.date: 10/29/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b84f603f185bd507111d4767a22e9009fc0e8b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430251"
---
# <a name="deploy-a-survivable-branch-appliance-or-server-with-lync-server-2013---branch-site-task"></a><span data-ttu-id="26699-103">Déploiement d’un Survivable Branch Appliance ou d’un serveur Survivable Branch Server sur un site de succursale avec Lync Server 2013 - tâche de site de succursale</span><span class="sxs-lookup"><span data-stu-id="26699-103">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26699-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26699-104">

<span> </span></span></span>

<span data-ttu-id="26699-105">_**Dernière modification de la rubrique :** 2014-10-28_</span><span class="sxs-lookup"><span data-stu-id="26699-105">_**Topic Last Modified:** 2014-10-28_</span></span>

<span data-ttu-id="26699-106">Effectuez l’une des deux procédures décrites dans cette rubrique sur le site de succursale, une fois que vous avez terminé les tâches de [déploiement d’une unité ou d’un serveur de succursales survivant avec Lync Server 2013-tâches de site central](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="26699-106">Perform one of the two procedures described in this topic at the branch site, after successfully completing the tasks in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="26699-107">Pour effectuer cette procédure, vous devez être membre du groupe RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="26699-107">To perform this procedure, you must be a member of the RTCUniversalSBATechnicians group.</span></span>



</div>

<div>

## <a name="to-deploy-the-survivable-branch-appliance"></a><span data-ttu-id="26699-108">Pour déployer l’application branche Survivable</span><span class="sxs-lookup"><span data-stu-id="26699-108">To deploy the Survivable Branch Appliance</span></span>

  - <span data-ttu-id="26699-109">Le déploiement de l’application branchement Survivable est activé par le fournisseur de l’appareil de succursale Survivable via une interface utilisateur Web.</span><span class="sxs-lookup"><span data-stu-id="26699-109">Survivable Branch Appliance deployment is enabled by the Survivable Branch Appliance vendor through a web user interface (UI).</span></span> <span data-ttu-id="26699-110">Pour plus d’informations sur le déploiement de l’application branche Survivable, consultez la documentation de votre fournisseur de solutions de branchement Survivable.</span><span class="sxs-lookup"><span data-stu-id="26699-110">For information about deploying the Survivable Branch Appliance, see your Survivable Branch Appliance vendor documentation.</span></span>

</div>

<div>

## <a name="to-deploy-the-survivable-branch-server"></a><span data-ttu-id="26699-111">Pour déployer le serveur de succursales survivant</span><span class="sxs-lookup"><span data-stu-id="26699-111">To deploy the Survivable Branch Server</span></span>

  - <span data-ttu-id="26699-112">Installez Lync Server 2013 sur un ordinateur exécutant Windows Server 2008 R2, Windows Server 2012 ou Windows Server 2012 R2, comme vous le feriez pour tout autre rôle serveur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="26699-112">Install Lync Server 2013 on a computer running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2, just as you would install any other Lync Server 2013 server role.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="26699-113">Pour plus d’informations sur l’installation de Lync Server, voir <A href="lync-server-2013-deploying-lync-server.md">déploiement de Lync server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="26699-113">For information about installing Lync Server, see <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="26699-114">**Étape suivante**: [configurer les utilisateurs pour la résilience du site de succursale dans Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span><span class="sxs-lookup"><span data-stu-id="26699-114">**Next step**: [Configuring users for branch site resiliency in Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="26699-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26699-115">See Also</span></span>


[<span data-ttu-id="26699-116">Annexe A : Utilisation d’applets de commande pour déployer un Survivable Branch Appliance dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26699-116">Appendix A: Using cmdlets to deploy a Survivable Branch Appliance in Lync Server 2013</span></span>](lync-server-2013-appendix-a-using-cmdlets-to-deploy-a-survivable-branch-appliance.md)  
  

<span data-ttu-id="26699-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26699-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

