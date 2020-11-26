---
title: 'Lync Server 2013 : suppression d’une stratégie d’archivage'
description: 'Lync Server 2013 : suppression d’une stratégie d’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving policy
ms:assetid: 4739a691-41cc-4128-8bb8-6d5a4c02107a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520989(v=OCS.15)
ms:contentKeyID: 48184043
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ecf465a62cf8f54777b03a1634d9a95f1b565c9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430363"
---
# <a name="deleting-an-archiving-policy-in-lync-server-2013"></a><span data-ttu-id="bb01a-103">Suppression d’une stratégie d’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb01a-103">Deleting an Archiving policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb01a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb01a-104">

<span> </span></span></span>

<span data-ttu-id="bb01a-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="bb01a-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="bb01a-106">Vous pouvez supprimer une stratégie d’utilisateur ou une stratégie de site.</span><span class="sxs-lookup"><span data-stu-id="bb01a-106">You can delete a user policy or site policy.</span></span> <span data-ttu-id="bb01a-107">La stratégie globale ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="bb01a-107">The global policy cannot be removed.</span></span> <span data-ttu-id="bb01a-108">Si vous tentez de supprimer la stratégie globale, Lync Server 2013 réinitialise automatiquement la stratégie aux valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb01a-108">If you try to delete the global policy, Lync Server 2013 automatically resets the policy to the default values.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bb01a-109">Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies Exchange contrôlent la mise en place de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="bb01a-109">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="bb01a-110">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="bb01a-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-delete-a-user-or-site-policy-for-archiving"></a><span data-ttu-id="bb01a-111">Pour supprimer une stratégie d’utilisateur ou de site pour l’archivage</span><span class="sxs-lookup"><span data-stu-id="bb01a-111">To delete a user or site policy for archiving</span></span>

1.  <span data-ttu-id="bb01a-112">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="bb01a-112">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bb01a-113">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="bb01a-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bb01a-114">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bb01a-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bb01a-115">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.</span><span class="sxs-lookup"><span data-stu-id="bb01a-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="bb01a-116">Dans la liste des stratégies d’archivage, cliquez sur la stratégie utilisateur ou la stratégie de site que vous souhaitez supprimer, cliquez sur **Modifier**, puis sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="bb01a-116">In the list of archiving policies, click the user or site policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="bb01a-117">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="bb01a-117">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="bb01a-118">Suppression de stratégies d’archivage à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb01a-118">Removing Archiving Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="bb01a-119">Les stratégies d’archivage peuvent être supprimées à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="bb01a-119">Archiving policies can be deleted by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="bb01a-120">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb01a-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="bb01a-121">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="bb01a-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-archiving-policy"></a><span data-ttu-id="bb01a-122">Pour supprimer une stratégie d’archivage spécifiée</span><span class="sxs-lookup"><span data-stu-id="bb01a-122">To remove a specified archiving policy</span></span>

  - <span data-ttu-id="bb01a-123">Par exemple, **Remove-CsArchivingPolicy** supprime la stratégie avec le site identité : Redmond.</span><span class="sxs-lookup"><span data-stu-id="bb01a-123">As an example, **Remove-CsArchivingPolicy** deletes the policy with the Identity site:Redmond.</span></span> <span data-ttu-id="bb01a-124">Notez qu’en cas de suppression d’une stratégie configurée sur l’étendue du site, les utilisateurs gérés par cette stratégie de site seront automatiquement gouvernés par la stratégie d’archivage globale.</span><span class="sxs-lookup"><span data-stu-id="bb01a-124">Note that, when a policy configured at the site scope is deleted, users previously managed by the site policy will automatically be governed by the global archiving policy instead.</span></span> <span data-ttu-id="bb01a-125">La commande suivante supprime l’archivage appliqué au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="bb01a-125">The following command removes the archiving applied to the Redmond site:</span></span>
    
        Remove-CsArchivingPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="bb01a-126">Pour supprimer toutes les stratégies d’archivage appliquées à l’étendue par utilisateur</span><span class="sxs-lookup"><span data-stu-id="bb01a-126">To remove all the archiving policies applied to the per-user scope</span></span>

  - <span data-ttu-id="bb01a-127">Cette commande supprime toutes les stratégies d’archivage appliquées à l’étendue par utilisateur :</span><span class="sxs-lookup"><span data-stu-id="bb01a-127">This command removes all the archiving policies applied to the per-user scope:</span></span>
    
        Get-CsArchivingPolicy -Filter "tag:*" | Remove-CsArchivingPolicy

</div>

<div>

## <a name="to-remove-all-the-archiving-policies-that-disable-internal-archiving"></a><span data-ttu-id="bb01a-128">Pour supprimer toutes les stratégies d’archivage qui désactivent l’archivage interne</span><span class="sxs-lookup"><span data-stu-id="bb01a-128">To remove all the archiving policies that disable internal archiving</span></span>

  - <span data-ttu-id="bb01a-129">Cette commande permet de supprimer toutes les stratégies d’archivage où l’archivage interne a été désactivé :</span><span class="sxs-lookup"><span data-stu-id="bb01a-129">This command removes all the archiving policies where internal archiving has been disabled:</span></span>
    
        Get-CsArchivingPolicy | Where-Object {$_.ArchiveInternal -eq $False} | Remove-CsArchivingPolicy

</div>

<span data-ttu-id="bb01a-130">Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="bb01a-130">For more information, see the help topic for the [Remove-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bb01a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb01a-131">See Also</span></span>


[<span data-ttu-id="bb01a-132">Gestion de l’archivage des communications internes et externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb01a-132">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="bb01a-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb01a-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

