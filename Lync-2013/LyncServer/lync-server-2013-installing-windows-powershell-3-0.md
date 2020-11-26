---
title: 'Lync Server 2013 : Installation de Windows PowerShell 3.0'
description: 'Lync Server 2013 : installation de Windows PowerShell 3,0.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Windows PowerShell 3.0
ms:assetid: d87bf21e-0a43-41cb-8fdc-626cedec8538
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205328(v=OCS.15)
ms:contentKeyID: 48185621
ms.date: 06/28/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4605231f4e73f6aada4fb34de895cdeb883d82b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426899"
---
# <a name="installing-windows-powershell-30-for-lync-server-2013"></a><span data-ttu-id="57cb6-103">Installation de Windows PowerShell 3.0 pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57cb6-103">Installing Windows PowerShell 3.0 for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57cb6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57cb6-104">

<span> </span></span></span>

<span data-ttu-id="57cb6-105">_**Dernière modification de la rubrique :** 2014-06-27_</span><span class="sxs-lookup"><span data-stu-id="57cb6-105">_**Topic Last Modified:** 2014-06-27_</span></span>

<span data-ttu-id="57cb6-106">Pour déployer Lync Server 2013 avec succès, vous avez besoin de Windows PowerShell 3,0 sur chaque ordinateur qui fait partie de la topologie de votre serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="57cb6-106">To deploy Lync Server 2013 successfully, you’ll need Windows PowerShell 3.0 on each computer that’s part of your Lync Server topology.</span></span>

<span data-ttu-id="57cb6-107">Pour le moment, pour les systèmes exécutant Windows Server 2012 ou Windows Server 2012 R2, vous n’avez pas besoin d’effectuer cette opération et vous pouvez passer à l’étape suivante du déploiement, car PowerShell 3,0 est inclus avec ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="57cb6-107">Now, for systems running Windows Server 2012 or Windows Server 2012 R2, you don’t need to do anything here, and can go ahead to the next stage of deployment, because PowerShell 3.0 is included with those operating systems.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="57cb6-108">Toutefois, pour les systèmes exécutant Windows Server 2008 R2 SP1, vous devez installer PowerShell 3,0 en tant que composant requis avant d’installer Lync Server 2013 ou les éléments ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="57cb6-108">But for systems running Windows Server 2008 R2 SP1, you’ll need to install PowerShell 3.0 as a prerequisite before you install Lync Server 2013, or things won’t work.</span></span> <span data-ttu-id="57cb6-109">Pour installer PowerShell 3,0, voir <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3,0</A>.</span><span class="sxs-lookup"><span data-stu-id="57cb6-109">To install PowerShell 3.0, see <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3.0</A>.</span></span> <span data-ttu-id="57cb6-110">Il s’agit d’un lien direct vers la page de téléchargement 3,0 PowerShell, ainsi que des informations relatives à son installation réussie.</span><span class="sxs-lookup"><span data-stu-id="57cb6-110">This is a direct link to the PowerShell 3.0 download page, along with information relating to installing it successfully.</span></span>



</div>

<span data-ttu-id="57cb6-111">Une fois l’installation terminée, ou si vous souhaitez simplement vérifier et être sûr d’avoir suivi le déploiement de Lync Server, il est très simple de vérifier que PowerShell 3,0 est sur un serveur si vous procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="57cb6-111">Once you’ve done the install, or if you just want to check and be sure before continuing with the Lync Server deployment, confirming that PowerShell 3.0 is on a server is pretty straightforward if you do this:</span></span>

1.  <span data-ttu-id="57cb6-112">Sur le serveur que vous voulez vérifier, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **accessoires**, sur **Windows PowerShell**, puis sur **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="57cb6-112">On the server you want to check, choose **Start**, click **All Programs**, click **Accessories**, click **Windows PowerShell**, and then click **Windows PowerShell**.</span></span>

2.  <span data-ttu-id="57cb6-113">Dans la console Windows PowerShell, tapez la commande suivante à l’invite de commandes, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="57cb6-113">In the Windows PowerShell console, type the following command at the command prompt, and then press ENTER:</span></span>
    
        Get-Host | Select-Object Version

3.  <span data-ttu-id="57cb6-114">Si Windows PowerShell 3,0 est installé, une sortie semblable à la suivante apparaît :</span><span class="sxs-lookup"><span data-stu-id="57cb6-114">If Windows PowerShell 3.0 is installed you’ll see output that looks like this:</span></span>
    
        Version
        -------
        3.0

<span data-ttu-id="57cb6-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57cb6-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

