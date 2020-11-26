---
title: 'Lync Server 2013 : supprimer un flux de travail'
description: 'Lync Server 2013 : supprimer un flux de travail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a workflow
ms:assetid: 0469a6b8-ce1e-459b-bc3d-4c8adf2d97d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520944(v=OCS.15)
ms:contentKeyID: 48183274
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a588a1dc0428660db95d4d492abbd1b157ca7a0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430650"
---
# <a name="delete-a-workflow-in-lync-server-2013"></a><span data-ttu-id="2b706-103">Supprimer un flux de travail dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b706-103">Delete a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b706-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b706-104">

<span> </span></span></span>

<span data-ttu-id="2b706-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2b706-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2b706-106">Pour supprimer un flux de travail, utilisez l’une des procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="2b706-106">Use one of the following procedures to delete a workflow.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-delete-a-workflow"></a><span data-ttu-id="2b706-107">Pour utiliser le panneau de configuration de Lync Server pour supprimer un flux de travail</span><span class="sxs-lookup"><span data-stu-id="2b706-107">To use Lync Server Control Panel delete a workflow</span></span>

1.  <span data-ttu-id="2b706-108">Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre de l’un des rôles d’administration prédéfinis prenant en charge Response Group.</span><span class="sxs-lookup"><span data-stu-id="2b706-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="2b706-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b706-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2b706-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2b706-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2b706-111">Dans la barre de navigation de gauche, cliquez sur **Services Response Group**, puis sur **Flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="2b706-111">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="2b706-112">Dans la page **Flux de travail**, cliquez sur **Créer ou modifier un flux de travail**.</span><span class="sxs-lookup"><span data-stu-id="2b706-112">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="2b706-113">Dans le champ de recherche **Sélectionner un service** , tapez tout ou partie du nom du service **ApplicationServer** qui héberge le flux de travail que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2b706-113">In the **Select a Service** search field, type part or all of the name of the **ApplicationServer** service that hosts the workflow that you want to delete.</span></span>

6.  <span data-ttu-id="2b706-114">Dans la liste de services, cliquez sur le service que vous souhaitez utiliser, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b706-114">In the list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="2b706-115">La page Web de l’outil de configuration de Response Group s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="2b706-115">The Response Group Configuration Tool webpage opens.</span></span> <span data-ttu-id="2b706-116">Vous pouvez également accéder à la page Web de l’outil de configuration du groupe de réponse directement à partir d’un navigateur Web en vous connectant à <STRONG>https:// &lt; webPoolFqdn &gt; /RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2b706-116">You can also open the Response Group Configuration Tool webpage directly from a web browser by connecting to <STRONG>https://&lt;webPoolFqdn&gt;/RgsConfig</STRONG>.</span></span>

    
    </div>

7.  <span data-ttu-id="2b706-117">Sous **gérer un flux de travail existant**, recherchez le flux de travail que vous voulez supprimer, puis sous **action**, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="2b706-117">Under **Manage an Existing Workflow**, locate the workflow you want to delete, and then under **Action**, click **Delete**.</span></span>

8.  <span data-ttu-id="2b706-118">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2b706-118">Click **Yes**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-workflow"></a><span data-ttu-id="2b706-119">Pour utiliser Windows PowerShell pour supprimer un flux de travail</span><span class="sxs-lookup"><span data-stu-id="2b706-119">To use Windows PowerShell to delete a workflow</span></span>

1.  <span data-ttu-id="2b706-120">Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre de l’un des rôles d’administration prédéfinis prenant en charge Response Group.</span><span class="sxs-lookup"><span data-stu-id="2b706-120">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="2b706-121">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="2b706-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2b706-122">Dans la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2b706-122">At the command line, run:</span></span>
    
        Get-CsRgsWorkflow -Identity <Application Server service> -Name "<name of workflow>" | Remove-CsRgsWorkflow
    
    <span data-ttu-id="2b706-123">Exemple :</span><span class="sxs-lookup"><span data-stu-id="2b706-123">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsWorkflow

<span data-ttu-id="2b706-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b706-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

