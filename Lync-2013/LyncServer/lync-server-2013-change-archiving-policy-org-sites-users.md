---
title: 'Lync Server 2013 : modification d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour votre organisation, certains sites ou des utilisateurs'
description: 'Lync Server 2013 : modification d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour votre organisation, vos sites ou vos utilisateurs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435179"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a><span data-ttu-id="ae1ea-103">Modification d’une stratégie d’archivage dans Lync Server 2013 pour activer ou désactiver l’archivage des communications internes ou externes pour votre organisation, certains sites ou des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ae1ea-103">Changing an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for your organization, sites, or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae1ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae1ea-104">

<span> </span></span></span>

<span data-ttu-id="ae1ea-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ae1ea-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ae1ea-106">Dans Lync Server 2013, vous utilisez des stratégies pour activer et désactiver l’archivage des communications internes et des communications externes pour les utilisateurs hébergés sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="ae1ea-107">Cela inclut les stratégies d’archivage suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="ae1ea-108">Stratégie globale créée par défaut lors du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="ae1ea-109">Stratégies de niveau de site et de niveau utilisateur facultatives que vous pouvez créer et utiliser pour spécifier la façon dont l’archivage est implémenté pour des sites ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="ae1ea-110">Vous définissez initialement des stratégies d’archivage lors du déploiement de l’archivage, mais vous pouvez modifier, ajouter et supprimer des stratégies après le déploiement.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="ae1ea-111">Dans Lync Server 2013 panneau de configuration, vous pouvez utiliser la page de **stratégie d’archivage** du groupe **archivage et surveillance** pour gérer les stratégies au niveau global, au niveau du site et au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="ae1ea-112">Si vous intégrez le stockage de votre serveur Lync au stockage 2013 Exchange, les stratégies d’utilisateur Exchange sont prioritaires sur les stratégies d’archivage de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="ae1ea-113">Pour plus d’informations sur l’implémentation de stratégies, y compris la hiérarchie des stratégies, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ae1ea-114">Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies Exchange contrôlent la mise en place de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-114">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ae1ea-115">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-115">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="ae1ea-116">Vous devez spécifier toutes les options appropriées dans les configurations d’archivage avant de procéder à l’archivage.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="ae1ea-117">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">la section gestion des options de configuration de l’archivage dans Lync Server 2013 pour votre organisation, vos sites et vos pools</A> dans la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span>



</div>

<div>

## <a name="to-change-an-archiving-policy"></a><span data-ttu-id="ae1ea-118">Pour modifier une stratégie d’archivage</span><span class="sxs-lookup"><span data-stu-id="ae1ea-118">To change an archiving policy</span></span>

1.  <span data-ttu-id="ae1ea-119">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-119">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ae1ea-120">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ae1ea-121">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ae1ea-122">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-122">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="ae1ea-123">Dans la liste des stratégies, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-123">In the list of policies, do one of the following:</span></span>
    
      - <span data-ttu-id="ae1ea-124">Pour modifier la stratégie pour l’ensemble de votre déploiement, cliquez sur **Globale** dans la liste des stratégies, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-124">To change the policy for your entire deployment, click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="ae1ea-125">Pour modifier la stratégie pour un seul site, cliquez sur le nom du site dans la liste des stratégies, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-125">To change the policy for a single site, click the site name in the list of policies, click **Edit**, and then click **Show details**.</span></span>
    
      - <span data-ttu-id="ae1ea-126">Pour modifier la stratégie pour un seul utilisateur ou groupe d’utilisateurs, cliquez sur l’utilisateur ou le groupe d’utilisateurs dans la liste des stratégies, sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-126">To change the policy for a single user or user group, click the user or user group name in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="ae1ea-127">Dans la page **Modifier la stratégie d’archivage**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-127">On the **Edit Archiving Policy** page, do the following:</span></span>
    
      - <span data-ttu-id="ae1ea-128">Pour activer ou désactiver l’archivage interne de la stratégie, activez ou désactivez la case à cocher **Archiver les communications internes**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-128">To enable or disable internal archiving for the policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="ae1ea-129">Pour activer ou désactiver l’archivage externe de la stratégie, activez ou désactivez la case à cocher **Archiver les communications externes**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-129">To enable or disable external archiving for the policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="ae1ea-130">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-130">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ae1ea-131">Les paramètres d’une stratégie utilisateur ne s’appliquent qu’aux utilisateurs et groupes d’utilisateurs spécifiques pour lesquels la stratégie a été définie.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-131">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="ae1ea-132">Pour plus d’informations, reportez-vous <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">à appliquer une stratégie d’archivage aux utilisateurs de Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="ae1ea-132">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ae1ea-133">Activation et désactivation de l’archivage à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae1ea-133">Enabling and Disabling Archiving by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ae1ea-134">Pour activer ou désactiver l’archivage, vous pouvez utiliser l’applet de cmdlet **Set-CsArchivingPolicy** pour les sessions internes et externes.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-134">Archiving can be enabled and disabled (for both internal and external communication sessions) by using the **Set-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="ae1ea-135">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-135">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ae1ea-136">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ae1ea-136">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a><span data-ttu-id="ae1ea-137">Pour activer l’archivage des sessions de communication internes</span><span class="sxs-lookup"><span data-stu-id="ae1ea-137">To enable the archiving of internal communication sessions</span></span>

  - <span data-ttu-id="ae1ea-138">Pour activer l’archivage des sessions de communication internes, définissez la valeur de la propriété **ArchiveInternal** sur True ($true).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-138">To enable archiving of internal communication sessions, set the value of the **ArchiveInternal** property to True ($True).</span></span> <span data-ttu-id="ae1ea-139">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-139">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a><span data-ttu-id="ae1ea-140">Pour activer l’archivage des sessions de communication externes</span><span class="sxs-lookup"><span data-stu-id="ae1ea-140">To enable the archiving of external communication sessions</span></span>

  - <span data-ttu-id="ae1ea-141">Pour activer l’archivage des sessions de communication externes, définissez la valeur de la propriété **ArchiveExternal** sur True ($true).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-141">To enable archiving of external communication sessions, set the value of the **ArchiveExternal** property to True ($True).</span></span> <span data-ttu-id="ae1ea-142">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-142">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="ae1ea-143">Pour activer l’archivage des sessions de communication interne et externe</span><span class="sxs-lookup"><span data-stu-id="ae1ea-143">To enable the archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="ae1ea-144">Pour activer l’archivage des sessions de communications internes et externes, définissez les propriétés **ArchiveInternal** et **ArchiveExternal** sur true :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-144">To enable archiving of both internal and external communications sessions, set both the **ArchiveInternal** and the **ArchiveExternal** properties to True:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a><span data-ttu-id="ae1ea-145">Pour désactiver l’archivage</span><span class="sxs-lookup"><span data-stu-id="ae1ea-145">To disable archiving</span></span>

  - <span data-ttu-id="ae1ea-146">Pour désactiver complètement l’archivage, définissez les propriétés **ArchiveInternal** et **ArchiveExternal** sur false ($false).</span><span class="sxs-lookup"><span data-stu-id="ae1ea-146">To disable archiving altogether, set both the **ArchiveInternal** and **ArchiveExternal** properties to False ($False).</span></span> <span data-ttu-id="ae1ea-147">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ae1ea-147">For example:</span></span>
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

<span data-ttu-id="ae1ea-148">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="ae1ea-148">For more information, see the help topic for the [Set-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ae1ea-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae1ea-149">See Also</span></span>


[<span data-ttu-id="ae1ea-150">Gestion de l’archivage des communications internes et externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae1ea-150">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="ae1ea-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae1ea-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

