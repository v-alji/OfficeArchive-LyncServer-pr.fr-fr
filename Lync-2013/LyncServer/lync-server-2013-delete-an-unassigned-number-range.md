---
title: 'Lync Server 2013 : supprimer une plage de numéros non affectée'
description: 'Lync Server 2013 : supprimez une plage de numéros non attribués.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an unassigned number range
ms:assetid: a8141bfb-b94d-4d0f-a7a9-2e60d10b103a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182565(v=OCS.15)
ms:contentKeyID: 48185090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 977cae1432c43a7df33e26597efdb364a7fbea08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430489"
---
# <a name="delete-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="83acf-103">Supprimer une plage de numéros non attribués dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83acf-103">Delete an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83acf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83acf-104">

<span> </span></span></span>

<span data-ttu-id="83acf-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="83acf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="83acf-106">Appliquez l’une des procédures suivantes pour supprimer une plage de numéros non attribués pour les annonces.</span><span class="sxs-lookup"><span data-stu-id="83acf-106">Use one of the following procedures to delete an unassigned number range for Announcements.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-unassigned-number-range"></a><span data-ttu-id="83acf-107">Pour utiliser le panneau de configuration de Lync Server pour supprimer une plage de numéros non attribués</span><span class="sxs-lookup"><span data-stu-id="83acf-107">To use Lync Server Control Panel to delete an unassigned number range</span></span>

1.  <span data-ttu-id="83acf-108">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="83acf-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="83acf-109">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="83acf-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="83acf-110">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="83acf-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="83acf-111">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="83acf-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="83acf-112">Dans la barre de navigation de gauche, cliquez sur **Fonctionnalités vocales**, puis sur **Numéro non attribué**.</span><span class="sxs-lookup"><span data-stu-id="83acf-112">In the left navigation bar, click **Voice Features** and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="83acf-113">Dans la page **Numéro non attribué**, dans le champ recherche, tapez entièrement ou partiellement le nom de la plage de numéros non attribués que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="83acf-113">On the **Unassigned Number** page, in the search field, type all or part of the name of the unassigned number range you want to delete.</span></span>

5.  <span data-ttu-id="83acf-114">Dans la liste des plages de numéros résultante, cliquez sur le nom, cliquez sur **Modifier**, puis sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="83acf-114">In the resulting list of number ranges, click the name, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="83acf-115">Cliquez sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="83acf-115">Click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-unassigned-number-range"></a><span data-ttu-id="83acf-116">Pour utiliser Windows PowerShell pour supprimer une plage de nombres non affectée</span><span class="sxs-lookup"><span data-stu-id="83acf-116">To use Windows PowerShell to delete an unassigned number range</span></span>

1.  <span data-ttu-id="83acf-117">Ouvrez une session sur l’ordinateur sur lequel Lync Server Management Shell est installé en tant que membre du groupe RTCUniversalServerAdmins ou avec les droits d’utilisateur nécessaires, comme décrit dans la rubrique [autorisations de configuration du délégué dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="83acf-117">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="83acf-118">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="83acf-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="83acf-119">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="83acf-119">At the command line, type:</span></span>
    
        Remove-CsUnassignedNumber -Identity "<name of unassigned number range>" 
    
    <span data-ttu-id="83acf-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="83acf-120">For example:</span></span>
    
        Remove-CsUnassignedNumber -Identity "Unassigned range 1"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="83acf-121">Pour plus d’informations sur les autres options, voir <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="83acf-121">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="83acf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83acf-122">See Also</span></span>


[<span data-ttu-id="83acf-123">Créer ou modifier une plage de nombres non affectées dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83acf-123">Create or modify an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-unassigned-number-range.md)  


[<span data-ttu-id="83acf-124">Remove-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="83acf-124">Remove-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUnassignedNumber)  
[<span data-ttu-id="83acf-125">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="83acf-125">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="83acf-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83acf-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

