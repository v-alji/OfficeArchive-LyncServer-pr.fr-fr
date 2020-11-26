---
title: 'Lync Server 2013 : application d’une stratégie d’archivage aux utilisateurs'
description: 'Lync Server 2013 : appliquer une stratégie d’archivage aux utilisateurs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Applying an Archiving policy to users
ms:assetid: 624a7d3e-389d-403a-97e5-f7bb17023ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521004(v=OCS.15)
ms:contentKeyID: 48184290
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54b82a68a75da7b389167097d8b08358cf680e1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439876"
---
# <a name="applying-an-archiving-policy-to-users-in-lync-server-2013"></a><span data-ttu-id="f4a7f-103">Appliquer une stratégie d’archivage aux utilisateurs de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4a7f-103">Applying an Archiving policy to users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4a7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4a7f-104">

<span> </span></span></span>

<span data-ttu-id="f4a7f-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f4a7f-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f4a7f-106">Si un utilisateur a été activé pour Lync Server 2013 et que vous avez créé une ou plusieurs stratégies utilisateur pour l’archivage pour les utilisateurs hébergés sur Lync Server 2013, vous pouvez implémenter la prise en charge de l’archivage pour des utilisateurs spécifiques en appliquant les stratégies appropriées aux utilisateurs ou groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-106">If a user has been enabled for Lync Server 2013 and you have created one or more user policies for archiving for users homed on Lync Server 2013, you can implement archiving support for specific users by applying the appropriate policies to those users or user groups.</span></span> <span data-ttu-id="f4a7f-107">Par exemple, si vous créez une stratégie pour la prise en charge de l’archivage des communications internes, vous pouvez l’appliquer à au moins un utilisateur ou groupe d’utilisateurs pour la prise en charge de l’archivage des communications Lync Server 2013 de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-107">For example, if you create a policy to support archiving of internal communications, you can apply it to at least one user or user group to support archiving of the user’s Lync Server 2013 communications.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f4a7f-108">Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies de blocage d' In-Place Exchange contrôlent l’activation de l’archivage pour les utilisateurs qui sont hébergés sur Exchange 2013 et dont leurs boîtes aux lettres sont placées sur In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-108">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="f4a7f-109">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-109">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="f4a7f-110">Vous devez spécifier toutes les options appropriées dans les configurations d’archivage avant de procéder à l’archivage.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-110">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="f4a7f-111">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">la section gestion des options de configuration de l’archivage dans Lync Server 2013 pour votre organisation, vos sites et vos pools</A> dans la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-111">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<span data-ttu-id="f4a7f-112">Suivez la procédure décrite dans cette rubrique pour appliquer une stratégie utilisateur d’archivage déjà créée à un ou plusieurs comptes d’utilisateurs ou groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-112">Use the procedure in this topic to apply a previously created Archiving user policy to one or more user accounts or user groups.</span></span>

<div>

## <a name="to-apply-an-archiving-user-policy-to-a-user-account"></a><span data-ttu-id="f4a7f-113">Pour appliquer une stratégie utilisateur d’archivage à un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f4a7f-113">To apply an archiving user policy to a user account</span></span>

1.  <span data-ttu-id="f4a7f-114">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f4a7f-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f4a7f-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f4a7f-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f4a7f-117">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**, puis recherchez le compte d’utilisateur que vous souhaitez configurer.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-117">In the left navigation bar, click **Users**, and then search for the user account that you want to configure.</span></span>

4.  <span data-ttu-id="f4a7f-118">Dans le tableau répertoriant les résultats de la recherche, cliquez sur le compte d’utilisateur, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-118">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f4a7f-119">Dans **modifier l’utilisateur de Lync Server** sous **stratégie d’archivage**, sélectionnez la stratégie d’utilisateur d’archivage que vous voulez appliquer.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-119">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f4a7f-120">Les paramètres <STRONG> &lt; automatiques &gt; </STRONG> appliquent les paramètres d’installation du serveur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-120">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings.</span></span> <span data-ttu-id="f4a7f-121">Ces paramètres sont appliqués automatiquement par le serveur.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-121">These settings are applied automatically by the server.</span></span>

    
    </div>

6.  <span data-ttu-id="f4a7f-122">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="assigning-a-per-user-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f4a7f-123">Attribution d’une stratégie d’archivage de Per-User à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4a7f-123">Assigning a Per-User Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f4a7f-124">Les stratégies d’archivage par utilisateur peuvent être affectées à l’aide de Windows PowerShell et de l’applet **de passe Grant-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="f4a7f-124">Per-user archiving policies can be assigned by using Windows PowerShell and the **Grant-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="f4a7f-125">Vous pouvez exécuter cette applet de commande à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-125">You can run this cmdlet from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f4a7f-126">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f4a7f-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-assign-a-per-user-archiving-policy-to-a-single-user"></a><span data-ttu-id="f4a7f-127">Pour attribuer une stratégie d’archivage par utilisateur à un utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="f4a7f-127">To assign a per-user archiving policy to a single user</span></span>

  - <span data-ttu-id="f4a7f-128">La commande suivante assigne la stratégie d’archivage par utilisateur RedmondArchivingPolicy à l’utilisateur Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-128">The following command assigns the per-user archiving policy RedmondArchivingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsArchivingPolicy -Identity "Ken Myer" -PolicyName "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-assign-a-per-user-archiving-policy-to-multiple-users"></a><span data-ttu-id="f4a7f-129">Pour attribuer une stratégie d’archivage par utilisateur à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f4a7f-129">To assign a per-user archiving policy to multiple users</span></span>

  - <span data-ttu-id="f4a7f-130">Cette commande affecte le RedmondArchivingPolicy de stratégie d’archivage par utilisateur à tous les utilisateurs disposant de comptes hébergés sur le pool d’inscriptions atl-cs-001.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-130">This command assigns the per-user archiving policy RedmondArchivingPolicy to all users who have accounts homed on the Registrar pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="f4a7f-131">Pour plus d’informations sur le paramètre de filtre utilisé dans cette commande, consultez la documentation sur l’applet de commande [Get-Csuser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="f4a7f-131">For details about the Filter parameter used in this command, see the [Get-CsUser](https://docs.microsoft.com/powershell/module/skype/Get-CsUser) cmdlet documentation.</span></span>
    
        Get-CsUser -Filter {RegistrarPool -eq "atl-cs-001.litwareinc.com"} | Grant-CsArchivingPolicy -PolicyName "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-assign-a-per-user-archiving-policy"></a><span data-ttu-id="f4a7f-132">Pour attribuer une stratégie d’archivage par utilisateur</span><span class="sxs-lookup"><span data-stu-id="f4a7f-132">To assign a per-user archiving policy</span></span>

  - <span data-ttu-id="f4a7f-133">La commande suivante réattribue toutes les stratégies d’archivage par utilisateur précédemment affectées à Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-133">The following command unassigns any per-user archiving policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="f4a7f-134">Une fois l’affectation de la stratégie par utilisateur annulée, Ken Myer sera automatiquement géré en utilisant la stratégie globale ou, le cas échéant, sa stratégie de site local.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-134">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="f4a7f-135">Une stratégie de site est prioritaire sur la stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="f4a7f-135">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsArchivingPolicy -Identity "Ken Myer" -PolicyName $Null

</div>

<span data-ttu-id="f4a7f-136">Pour plus d’informations, reportez-vous à la documentation sur l’applet [de passe Grant-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="f4a7f-136">For details, see the [Grant-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsArchivingPolicy) cmdlet documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f4a7f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a7f-137">See Also</span></span>


[<span data-ttu-id="f4a7f-138">Gestion de l’archivage des communications internes et externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4a7f-138">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
[<span data-ttu-id="f4a7f-139">Attribution de stratégies par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4a7f-139">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)  
  

<span data-ttu-id="f4a7f-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4a7f-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

