---
title: 'Lync Server 2013 : supprimer une stratégie de version de client existante'
description: 'Lync Server 2013 : supprimez une stratégie de version de client existante.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing client version policy
ms:assetid: b88aaa25-97ff-4eb6-bd34-b97332cd6890
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923064(v=OCS.15)
ms:contentKeyID: 50675349
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1328d54790b2a7856fa2776bb59feeb515bab1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430601"
---
# <a name="delete-an-existing-client-version-policy-in-lync-server-2013"></a><span data-ttu-id="af880-103">Supprimer une stratégie de version de client existante dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="af880-103">Delete an existing client version policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af880-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af880-104">

<span> </span></span></span>

<span data-ttu-id="af880-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="af880-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="af880-106">Si vous souhaitez supprimer une stratégie de version de client déjà configurée, vous pouvez la supprimer de Lync Server 2013 Control Panel ou de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="af880-106">If you want to delete a client version policy that was previously configured, you can delete it from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-delete-client-version-policies-by-using-lync-server-control-panel"></a><span data-ttu-id="af880-107">Pour supprimer les stratégies de version du client à l’aide du panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="af880-107">To delete client version policies by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="af880-108">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="af880-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="af880-109">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="af880-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="af880-110">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="af880-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="af880-111">Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton de navigation de la stratégie de la **version de client** .</span><span class="sxs-lookup"><span data-stu-id="af880-111">In the left navigation bar, click **Clients**, and then click the **Client Version Policy** navigation button.</span></span>

4.  <span data-ttu-id="af880-112">Dans la page de **stratégie de version du client** , sélectionnez la ou les stratégies de version de client à supprimer, cliquez sur **modifier**, puis sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="af880-112">On the **Client Version Policy** page, select the client version policy or policies you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="deleting-client-version-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="af880-113">Suppression de stratégies de version du client à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="af880-113">Deleting Client Version Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="af880-114">Vous pouvez supprimer des stratégies de version du client à l’aide de l’applet de contrôle **Remove-CsClientVersionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="af880-114">You can delete client version policies by using the **Remove-CsClientVersionPolicy** cmdlet.</span></span> <span data-ttu-id="af880-115">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="af880-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="af880-116">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="af880-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-client-version-policy"></a><span data-ttu-id="af880-117">Pour supprimer une stratégie de version de client spécifique</span><span class="sxs-lookup"><span data-stu-id="af880-117">To remove a specific client version policy</span></span>

  - <span data-ttu-id="af880-118">Cette commande supprime la stratégie de version du client appliquée au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="af880-118">This command deletes the client version policy applied to the Redmond site:</span></span>
    
        Remove-CsClientVersionPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-client-version-policies-applied-to-the-site-scope"></a><span data-ttu-id="af880-119">Pour supprimer toutes les stratégies de version de client appliquées à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="af880-119">To remove all the client version policies applied to the site scope</span></span>

  - <span data-ttu-id="af880-120">Cette commande supprime toutes les stratégies de version de client configurées sur l’étendue du site :</span><span class="sxs-lookup"><span data-stu-id="af880-120">This command removes all the client version policies configured at the site scope:</span></span>
    
        Get-CsClientVersionPolicy -Fiter "site:*" | Remove-CsClientVersionPolicy

</div>

<div>

## <a name="to-remove-client-version-policies-that-do-not-include-a-specific-user-agent"></a><span data-ttu-id="af880-121">Pour supprimer les stratégies de version de client n’incluant pas d’agent utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="af880-121">To remove client version policies that do not include a specific user agent</span></span>

  - <span data-ttu-id="af880-122">Cette commande supprime toutes les stratégies de version de client n’incluant pas de règle pour l’agent utilisateur de Lync pour Windows Phone (WPLync) :</span><span class="sxs-lookup"><span data-stu-id="af880-122">And this command removes any client version policies that do not include a rule for the Windows Phone Lync (WPLync) user agent:</span></span>
    
        Get-CsClientVersionPolicy | Where-Object {$_.Rules -notmatch "UserAgent=WPLync" | Remove-CsClientVersionPolicy

</div>

<span data-ttu-id="af880-123">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Remove-CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) .</span><span class="sxs-lookup"><span data-stu-id="af880-123">For details, see the Help topic for the [Remove-CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) cmdlet.</span></span>

<span data-ttu-id="af880-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af880-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

