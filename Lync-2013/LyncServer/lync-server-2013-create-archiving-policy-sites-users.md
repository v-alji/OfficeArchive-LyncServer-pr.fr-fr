---
title: 'Lync Server 2013 : création d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques'
description: 'Lync Server 2013 : création d’une stratégie d’archivage pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431987"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a><span data-ttu-id="c5843-103">Création d’une stratégie d’archivage dans Lync Server 2013 pour activer ou désactiver l’archivage des communications internes ou externes pour des sites ou des utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="c5843-103">Creating an Archiving policy in Lync Server 2013 to enable or disable Archiving of internal or external communications for specific sites or users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5843-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5843-104">

<span> </span></span></span>

<span data-ttu-id="c5843-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="c5843-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="c5843-106">Dans Lync Server 2013, vous utilisez des stratégies pour activer et désactiver l’archivage des communications internes et des communications externes pour les utilisateurs hébergés sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5843-106">In Lync Server 2013, you use policies to enable and disable archiving for internal communications and external communications for users homed on Lync Server 2013.</span></span> <span data-ttu-id="c5843-107">Cela inclut les stratégies d’archivage suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5843-107">This includes the following Archiving policies:</span></span>

  - <span data-ttu-id="c5843-108">Stratégie globale créée par défaut lors du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5843-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="c5843-109">Stratégies de niveau de site et de niveau utilisateur facultatives que vous pouvez créer et utiliser pour spécifier la façon dont l’archivage est implémenté pour des sites ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c5843-109">Optional site-level and user-level policies that you can create and use to specify how archiving is implemented for specific sites or users.</span></span>

<span data-ttu-id="c5843-110">Vous définissez initialement des stratégies d’archivage lors du déploiement de l’archivage, mais vous pouvez modifier, ajouter et supprimer des stratégies après le déploiement.</span><span class="sxs-lookup"><span data-stu-id="c5843-110">You initially set up Archiving policies when you deploy Archiving, but you can change, add, and delete policies after deployment.</span></span> <span data-ttu-id="c5843-111">Dans Lync Server 2013 panneau de configuration, vous pouvez utiliser la page de **stratégie d’archivage** du groupe **archivage et surveillance** pour gérer les stratégies au niveau global, au niveau du site et au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c5843-111">In Lync Server 2013 Control Panel, you can use the **Archiving Policy** page of the **Archiving and Monitoring** group to manage policies at the global level, site level, and user level.</span></span> <span data-ttu-id="c5843-112">Si vous intégrez le stockage de votre serveur Lync au stockage 2013 Exchange, les stratégies d’utilisateur Exchange sont prioritaires sur les stratégies d’archivage de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5843-112">If you integrate your Lync Server storage with Exchange 2013 storage, the Exchange user policies take precedence over the Lync Server 2013 archiving policies.</span></span>

<span data-ttu-id="c5843-113">Pour plus d’informations sur l’implémentation de stratégies, y compris la hiérarchie des stratégies, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.</span><span class="sxs-lookup"><span data-stu-id="c5843-113">For details about how policies are implemented, including the hierarchy of policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="c5843-114">Pour contrôler l’implémentation de l’archivage, vous devez spécifier les options de configuration de l’archivage, par exemple pour archiver les messages instantanés ou les conférences, utiliser le mode Critical et les options de purge.</span><span class="sxs-lookup"><span data-stu-id="c5843-114">To control the implementation of Archiving, you must specify options in Archiving configurations, such as whether to archive IM or conferencing, the use of critical mode, and purging options.</span></span> <span data-ttu-id="c5843-115">Par défaut, aucune option n’est activée dans la configuration de l’archivage global ni dans toute configuration d’archivage de site ou de pool.</span><span class="sxs-lookup"><span data-stu-id="c5843-115">By default no options are enabled in the global Archiving configuration or any site or pool Archiving configuration.</span></span> <span data-ttu-id="c5843-116">Vous devez spécifier toutes les options appropriées dans les configurations d’archivage avant de procéder à l’archivage des communications internes ou externes dans les stratégies d’archivage.</span><span class="sxs-lookup"><span data-stu-id="c5843-116">You should specify all appropriate options in the Archiving configurations before enabling Archiving for internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="c5843-117">Pour plus d’informations, reportez-vous à <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">la section gestion des options de configuration de l’archivage dans Lync Server 2013 pour votre organisation, vos sites et vos pools</A> dans la documentation des opérations.</span><span class="sxs-lookup"><span data-stu-id="c5843-117">For details, see <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</A> in the Operations documentation.</span></span><BR><span data-ttu-id="c5843-118">Si vous avez activé l’intégration de Microsoft Exchange pour votre déploiement, les stratégies Exchange contrôlent la mise en place de l’archivage pour les utilisateurs hébergés sur Exchange 2013 et disposant de leurs boîtes aux lettres dans In-Place attente.</span><span class="sxs-lookup"><span data-stu-id="c5843-118">If you enabled Microsoft Exchange integration for your deployment, Exchange policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="c5843-119">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">configuration de stratégies d’archivage dans Lync server 2013 lors de l’utilisation d’une intégration Exchange Server</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="c5843-119">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a><span data-ttu-id="c5843-120">Pour créer une stratégie d’archivage pour un site ou des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c5843-120">To create an archiving policy for a site or users</span></span>

1.  <span data-ttu-id="c5843-121">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="c5843-121">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c5843-122">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c5843-122">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c5843-123">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c5843-123">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c5843-124">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **stratégie d’archivage**.</span><span class="sxs-lookup"><span data-stu-id="c5843-124">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="c5843-125">Cliquez sur **Nouveau**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5843-125">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="c5843-126">Pour créer une stratégie d’archivage au niveau du site, cliquez sur **stratégie de site** , puis dans **Sélectionner un site**, cliquez sur le site auquel vous voulez appliquer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c5843-126">To create a site-level archiving policy, click **Site policy** and then, in **Select a site**, click the site to which the policy is to be applied.</span></span>
    
      - <span data-ttu-id="c5843-127">Pour créer une stratégie d’archivage au niveau de l’utilisateur, cliquez sur **Stratégie de l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="c5843-127">To create a user-level archiving policy, click **User policy**.</span></span>

5.  <span data-ttu-id="c5843-128">Dans **Nouvelle stratégie d’archivage**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5843-128">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="c5843-129">Dans **Nom**, spécifiez un nom pour la nouvelle stratégie (par exemple, externalContoso).</span><span class="sxs-lookup"><span data-stu-id="c5843-129">In **Name**, specify a name for the new policy (for example, externalContoso).</span></span>
    
      - <span data-ttu-id="c5843-130">Dans **Description**, entrez des informations décrivant la stratégie (par exemple, stratégie d’archivage des utilisateurs externes pour Contoso).</span><span class="sxs-lookup"><span data-stu-id="c5843-130">In **Description**, provide details about what the policy is (for example, External user archiving policy for Contoso).</span></span>
    
      - <span data-ttu-id="c5843-131">Pour contrôler l’archivage des communications avec les utilisateurs internes, activez ou désactivez la case à cocher **Archiver les communications internes**.</span><span class="sxs-lookup"><span data-stu-id="c5843-131">To control archiving of communications with internal users, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="c5843-132">Pour contrôler l’archivage des communications avec les utilisateurs externes, activez ou désactivez la case à cocher **Archiver les communications externes**.</span><span class="sxs-lookup"><span data-stu-id="c5843-132">To control archiving of communications with external users, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="c5843-133">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="c5843-133">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="c5843-134">Les paramètres d’une stratégie utilisateur ne s’appliquent qu’aux utilisateurs et groupes d’utilisateurs spécifiques pour lesquels la stratégie a été définie.</span><span class="sxs-lookup"><span data-stu-id="c5843-134">The settings of a user policy only apply to the specific users and user groups to which you apply the policy.</span></span> <span data-ttu-id="c5843-135">Pour plus d’informations, reportez-vous <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">à appliquer une stratégie d’archivage aux utilisateurs de Lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="c5843-135">For details, see <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Applying an Archiving policy to users in Lync Server 2013</A></span></span>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="c5843-136">Création d’une stratégie d’archivage à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5843-136">Creating an Archiving Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="c5843-137">Les stratégies d’archivage peuvent être créées à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsArchivingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="c5843-137">Archiving policies can be created by using Windows PowerShell and the **Remove-CsArchivingPolicy** cmdlet.</span></span> <span data-ttu-id="c5843-138">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5843-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="c5843-139">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="c5843-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a><span data-ttu-id="c5843-140">Pour créer une nouvelle stratégie d’archivage à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="c5843-140">To create a new archiving policy at the site scope</span></span>

  - <span data-ttu-id="c5843-141">Cette commande crée une stratégie d’archivage pour le site Redmond :</span><span class="sxs-lookup"><span data-stu-id="c5843-141">This command creates a new archiving policy for the Redmond site:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a><span data-ttu-id="c5843-142">Pour créer une nouvelle stratégie d’archivage à l’étendue de chaque utilisateur</span><span class="sxs-lookup"><span data-stu-id="c5843-142">To create a new archiving policy at the per-user scope</span></span>

  - <span data-ttu-id="c5843-143">Pour créer une nouvelle stratégie d’archivage à l’étendue par utilisateur, spécifiez simplement une identité unique lors de la création de la stratégie :</span><span class="sxs-lookup"><span data-stu-id="c5843-143">To create a new archiving policy at the per-user scope, simply specify a unique Identity when creating the policy:</span></span>
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a><span data-ttu-id="c5843-144">Pour créer une nouvelle stratégie d’archivage qui permet d’archiver des sessions de communication interne</span><span class="sxs-lookup"><span data-stu-id="c5843-144">To create a new archiving policy that enables archiving of internal communication sessions</span></span>

  - <span data-ttu-id="c5843-145">Dans la mesure où aucun paramètre (à l’exception du paramètre obligatoire Identity) n’a été spécifié dans les commandes précédentes, les nouvelles stratégies utilisent les valeurs par défaut pour toutes leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="c5843-145">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding commands, the new policies will use the default values for all their properties.</span></span> <span data-ttu-id="c5843-146">Pour créer des stratégies qui utilisent des valeurs de propriétés distinctes, il vous suffit d’inclure le paramètre et la valeur de paramètre appropriés.</span><span class="sxs-lookup"><span data-stu-id="c5843-146">To create policies that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="c5843-147">Par exemple, pour créer une stratégie d’archivage qui permet l’archivage des sessions de messagerie instantanée internes, utilisez une commande comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="c5843-147">For example, to create an archiving policy that permits archiving of internal instant messaging sessions use a command like this:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a><span data-ttu-id="c5843-148">Pour créer une nouvelle stratégie d’archivage qui permet d’archiver des sessions de communication interne et externe</span><span class="sxs-lookup"><span data-stu-id="c5843-148">To create a new archiving policy that enables archiving of both internal and external communication sessions</span></span>

  - <span data-ttu-id="c5843-149">Vous pouvez modifier plusieurs valeurs de propriétés en incluant plusieurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="c5843-149">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="c5843-150">Par exemple, cette commande configure la nouvelle stratégie d’archivage des sessions de messagerie instantanée internes et externes :</span><span class="sxs-lookup"><span data-stu-id="c5843-150">For example, this command configures the new policy to archiving both internal and external instant messaging sessions:</span></span>
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

<span data-ttu-id="c5843-151">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de [nouvelle-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="c5843-151">For more information, see the help topic for the [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c5843-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5843-152">See Also</span></span>


[<span data-ttu-id="c5843-153">Gestion de l’archivage des communications internes et externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5843-153">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="c5843-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5843-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

