---
title: 'Lync Server 2013 : affecter une stratégie de conférence par utilisateur'
description: 'Lync Server 2013 : attribuez une stratégie de conférence par utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user conferencing policy
ms:assetid: 72f12c72-65f7-44fe-ab81-0f57cb2f87d1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521015(v=OCS.15)
ms:contentKeyID: 48184475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819d1431a2a7a921ff8c306c47c8b5f86bf5d5bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440513"
---
# <a name="assign-a-per-user-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="886bf-103">Affecter une stratégie de conférence par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="886bf-103">Assign a per-user conferencing policy in Lync Server 2013</span></span>

 


<span data-ttu-id="886bf-104">La stratégie de conférence est l’un des paramètres individuels d’un compte d’utilisateur que vous pouvez configurer dans le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="886bf-104">The conferencing policy is one of the individual settings of a user account that you can configure in Lync Server Control Panel.</span></span>

<span data-ttu-id="886bf-105">Le déploiement d’une ou plusieurs stratégies de conférence par utilisateur est facultatif.</span><span class="sxs-lookup"><span data-stu-id="886bf-105">Deploying one or more per-user conferencing policies is optional.</span></span> <span data-ttu-id="886bf-106">Vous pouvez également déployer uniquement une stratégie de conférence de niveau global ou une stratégie de conférence au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="886bf-106">You can also deploy only a global-level conferencing policy or site-level conferencing policy.</span></span> <span data-ttu-id="886bf-107">Si vous déployez des stratégies par utilisateur, vous devez les affecter explicitement aux utilisateurs, groupes ou objets de contact.</span><span class="sxs-lookup"><span data-stu-id="886bf-107">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span> <span data-ttu-id="886bf-108">Les autorisations et privilèges d’utilisateur de la Conférence par défaut sont automatiquement définis dans la stratégie de conférence au niveau global lorsqu’aucune stratégie spécifique de niveau de site ou d’utilisateur n’est affectée.</span><span class="sxs-lookup"><span data-stu-id="886bf-108">Conferencing user rights and permissions automatically default to those defined in the global-level conferencing policy when no specific site-level or per-user policy is assigned.</span></span>

<span data-ttu-id="886bf-109">Après avoir créé au moins une stratégie de conférence par utilisateur, suivez les procédures décrites dans cette rubrique pour affecter la stratégie qui spécifie les droits d’utilisateur et les autorisations que le serveur doit accorder aux réunions organisées par un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="886bf-109">After creating at least one per-user conferencing policy, use the procedures in this topic to assign the policy that specifies the user rights and permissions that you want the server to grant to the meetings organized by a particular user.</span></span>

<span data-ttu-id="886bf-110">Pour obtenir la liste de tous les paramètres de stratégie de conférence disponibles, voir [référence des paramètres de stratégie de conférence pour Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="886bf-110">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<span data-ttu-id="886bf-111">Pour plus d’informations sur la création de stratégies de conférence, voir [créer ou modifier une stratégie de conférence dans Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="886bf-111">For details about creating conferencing policies, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy"></a><span data-ttu-id="886bf-112">Pour attribuer une stratégie de conférence par utilisateur</span><span class="sxs-lookup"><span data-stu-id="886bf-112">To assign a per-user conferencing policy</span></span>

1.  <span data-ttu-id="886bf-113">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="886bf-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="886bf-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="886bf-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="886bf-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="886bf-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="886bf-116">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="886bf-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="886bf-117">Recherchez un utilisateur à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="886bf-117">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="886bf-118">Dans la zone **Rechercher des utilisateurs**, tapez le début ou l’intégralité du nom d’affichage, du prénom, du nom de famille, du nom de compte SAM, de l’adresse SIP (Session Initiation Protocol) ou de l’URI de ligne du compte d’utilisateur, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="886bf-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="886bf-119">Si vous avez enregistré une requête, cliquez sur l’icône **Ouvrir une requête**, puis sur **Rechercher** dans la boîte de dialogue **Ouvrir** pour rechercher la requête (un fichier .usf).</span><span class="sxs-lookup"><span data-stu-id="886bf-119">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="886bf-120">(Facultatif) Indiquez des critères de recherche supplémentaires pour affiner les résultats :</span><span class="sxs-lookup"><span data-stu-id="886bf-120">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="886bf-121">Cliquez sur **Ajouter un filtre**.</span><span class="sxs-lookup"><span data-stu-id="886bf-121">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="886bf-122">Entrez la propriété utilisateur en tapant son nom ou en cliquant sur la flèche de la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="886bf-122">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="886bf-123">Dans la liste déroulante **Égal à**, cliquez sur l’opérateur (par exemple, **Égal à** ou **Pas égal à**).</span><span class="sxs-lookup"><span data-stu-id="886bf-123">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="886bf-124">Selon la propriété utilisateur que vous avez sélectionnée, entrez le critère que vous souhaitez utiliser pour filtrer les résultats de recherche en le tapant ou en cliquant sur la flèche dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="886bf-124">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="886bf-125">Pour ajouter des clauses de recherche supplémentaires à la requête, cliquez sur <STRONG>Ajouter un filtre</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="886bf-125">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="886bf-126">Cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="886bf-126">Click **Find**.</span></span>

6.  <span data-ttu-id="886bf-127">Cliquez sur un utilisateur dans les résultats, puis sur **Action** et sur **Attribuer des stratégies**.</span><span class="sxs-lookup"><span data-stu-id="886bf-127">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="886bf-128">Si vous voulez appliquer la même stratégie de conférence par utilisateur à plusieurs utilisateurs, sélectionnez plusieurs utilisateurs dans les résultats de la recherche, cliquez sur <STRONG>actions</STRONG>, puis sur <STRONG>affecter des stratégies</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="886bf-128">If you want the same per-user conferencing policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="886bf-129">Dans **affecter des stratégies**, sous **stratégie de conférence**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="886bf-129">In **Assign Policies**, under **Conferencing policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="886bf-130">Dans la mesure où il existe plusieurs stratégies que vous pouvez configurer dans <STRONG>affecter des stratégies</STRONG>, l’option <STRONG> &lt; &gt; rester en</STRONG> cours est activée par défaut pour chaque stratégie dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="886bf-130">Because there are multiple policies that you can configure in <STRONG>Assign Policies</STRONG>, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="886bf-131">Continuez à utiliser la stratégie précédemment attribuée à l’utilisateur sans apporter de modification au paramètre.</span><span class="sxs-lookup"><span data-stu-id="886bf-131">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="886bf-132">Activez cette option **\<Automatic\>** pour autoriser Lync Server 2013 à choisir automatiquement la stratégie de niveau global ou, s’il est défini, la stratégie au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="886bf-132">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="886bf-133">Cliquez sur le nom d’une stratégie de conférence par utilisateur que vous avez précédemment définie dans la page **stratégie de conférence** .</span><span class="sxs-lookup"><span data-stu-id="886bf-133">Click the name of a per-user conferencing policy you previously defined on the **Conferencing Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="886bf-134">Pour vous aider à décider quelle stratégie attribuer, après avoir cliqué sur un nom de stratégie, cliquez sur <STRONG>Afficher</STRONG> pour afficher les droits et autorisations des utilisateurs définis dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="886bf-134">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="886bf-135">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="886bf-135">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-conferencing-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="886bf-136">Attribution d’une stratégie de conférence Per-User à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="886bf-136">Assigning a Per-User Conferencing Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="886bf-137">Les stratégies de conférence par utilisateur peuvent être affectées à l’aide de Windows PowerShell et de l’applet de Grant-CsConferencingPolicy.</span><span class="sxs-lookup"><span data-stu-id="886bf-137">Per-user conferencing policies can be assigned by using Windows PowerShell and the Grant-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="886bf-138">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="886bf-138">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="886bf-139">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="886bf-139">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-conferencing-policy-to-a-single-user"></a><span data-ttu-id="886bf-140">Pour attribuer une stratégie de conférence par utilisateur à un utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="886bf-140">To assign a per-user conferencing policy to a single user</span></span>

  - <span data-ttu-id="886bf-141">La commande suivante affecte le RedmondConferencingPolicy de stratégie de conférence par utilisateur à l’utilisateur Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="886bf-141">The following command assigns the per-user conferencing policy RedmondConferencingPolicy to the user Ken Myer.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName "RedmondConferencingPolicy"

## <a name="to-assign-a-per-user-conferencing-policy-to-multiple-users"></a><span data-ttu-id="886bf-142">Pour attribuer une stratégie de conférence par utilisateur à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="886bf-142">To assign a per-user conferencing policy to multiple users</span></span>

  - <span data-ttu-id="886bf-143">Cette commande affecte la stratégie de conférence HRConferencingPolicy à tous les utilisateurs qui travaillent pour le service de ressources humaines.</span><span class="sxs-lookup"><span data-stu-id="886bf-143">This command assigns the per-user conferencing policy HRConferencingPolicy to all the users who work for the Human Resources department.</span></span> <span data-ttu-id="886bf-144">Pour plus d’informations sur le paramètre LdapFilter utilisé dans cette commande, voir la documentation relative à l’applet de commande [Get-Csuser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="886bf-144">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=Human Resources" | Grant-CsConferencingPolicy -PolicyName "HRConferencingPolicy"

## <a name="to-unassign-a-per-user-conferencing-policy"></a><span data-ttu-id="886bf-145">Pour annuler l’affectation d’une stratégie de conférence par utilisateur</span><span class="sxs-lookup"><span data-stu-id="886bf-145">To unassign a per-user conferencing policy</span></span>

  - <span data-ttu-id="886bf-146">La commande suivante annule l’attribution d’une stratégie de conférence par utilisateur précédemment attribuée à Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="886bf-146">The following command unassigns any per-user conferencing policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="886bf-147">Une fois l’affectation de la stratégie par utilisateur annulée, Ken Myer sera automatiquement géré en utilisant la stratégie globale ou, le cas échéant, sa stratégie de site local.</span><span class="sxs-lookup"><span data-stu-id="886bf-147">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="886bf-148">Une stratégie de site est prioritaire sur la stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="886bf-148">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsConferencingPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="886bf-149">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="886bf-149">For more information, see the help topic for the [Grant-CsConferencingPolicy](https://technet.microsoft.com/library/gg425937\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="886bf-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="886bf-150">See Also</span></span>


[<span data-ttu-id="886bf-151">Création ou modification d’une stratégie de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="886bf-151">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)  


[<span data-ttu-id="886bf-152">Attribution de stratégies par utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="886bf-152">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

