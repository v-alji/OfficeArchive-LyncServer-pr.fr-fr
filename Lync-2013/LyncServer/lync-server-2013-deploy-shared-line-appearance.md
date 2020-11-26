---
title: 'Lync Server 2013 : déploiement de l’apparence des lignes partagées'
description: 'Lync Server 2013 : déploiement de l’apparence des lignes partagées.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy Shared Line Appearance
ms:assetid: 6666dfef-9ecf-4834-af6a-2d5da227dfa3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Mt712152(v=OCS.15)
ms:contentKeyID: 72522137
ms.date: 06/13/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c83c06bbc9b91e11cabc0abee20de28fc7281205
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430174"
---
# <a name="deploy-shared-line-appearance-in-lync-server-2013"></a><span data-ttu-id="bb3d6-103">Déploiement de l’apparence des lignes partagées dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb3d6-103">Deploy Shared Line Appearance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb3d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb3d6-104">

<span> </span></span></span>

<span data-ttu-id="bb3d6-105">_**Dernière modification de la rubrique :** 2016-06-13_</span><span class="sxs-lookup"><span data-stu-id="bb3d6-105">_**Topic Last Modified:** 2016-06-13_</span></span>

<span data-ttu-id="bb3d6-106">Pour plus d’informations sur le déploiement de l’apparence des lignes partagées dans Lync Server 2013, consultez la mise à jour cumulative 2016.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-106">Read this topic to learn how to deploy Shared Line Appearance (SLA) in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="bb3d6-107">Le mode partage de lignes est une fonctionnalité permettant de gérer plusieurs appels sur un numéro spécifique appelé « numéro partagé ».</span><span class="sxs-lookup"><span data-stu-id="bb3d6-107">SLA is a feature for handling multiple calls on a specific number called a shared number.</span></span>

<span data-ttu-id="bb3d6-108">Pour plus d’informations sur cette fonctionnalité, voir [planifier l’apparition de lignes partagées dans Lync Server 2013](lync-server-2013-plan-for-shared-line-appearance.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d6-108">For more information about this feature, see [Plan for Shared Line Appearance in Lync Server 2013](lync-server-2013-plan-for-shared-line-appearance.md).</span></span>

<span data-ttu-id="bb3d6-109">L’apparence des lignes partagées (SLA) est une nouvelle fonctionnalité de Lync Server 2013, mise à jour cumulative 2016.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-109">Shared Line Appearance (SLA) is a new feature in Lync Server 2013, Cumulative Update April 2016.</span></span> <span data-ttu-id="bb3d6-110">Pour activer cette fonctionnalité, vous devez d’abord avoir déployé cette mise à jour cumulative.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-110">To enable this feature, you must have first deployed this cumulative update.</span></span>

<div>

## <a name="install-shared-line-appearance"></a><span data-ttu-id="bb3d6-111">Installation du mode partage de lignes</span><span class="sxs-lookup"><span data-stu-id="bb3d6-111">Install Shared Line Appearance</span></span>

1.  <span data-ttu-id="bb3d6-112">Après le déploiement de Lync Server 2013, la mise à jour cumulative 2016 avril est déployée, l’application SLA n’est pas activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-112">After Lync Server 2013, Cumulative Update April 2016 is deployed, the SLA application is not enabled by default.</span></span> <span data-ttu-id="bb3d6-113">Pour activer l’application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-113">To enable the application, follow the steps below:</span></span>
    
    1.  <span data-ttu-id="bb3d6-114">Enregistrez le mode partage de lignes comme application serveur en exécutant la commande ci-dessous pour chaque pool :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-114">Register SLA as a server application by running the following command for each pool:</span></span>
        ```powershell
        New-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/SharedLineAppearance' -Uri
                        http://www.microsoft.com/LCS/SharedLineAppearance -Critical $false -Enabled
                        $true -Priority (Get-CsServerApplication -Identity
                        'Service:Registrar:%FQDN%/UserServices').Priority 
        ```
        <span data-ttu-id="bb3d6-115">où %FQDN% est le nom de domaine complet du pool.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-115">where %FQDN% is the fully qualified domain name of the pool.</span></span>
    
    2.  <span data-ttu-id="bb3d6-116">Exécutez la commande ci-dessous pour mettre à jour les rôles RBAC pour les applets de commande du mode partage de lignes :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-116">Run the following command to update the RBAC roles for the SLA cmdlets:</span></span>
        ```powershell
        Update-CsAdminRole 
        ```
    3.  <span data-ttu-id="bb3d6-117">Redémarrez tous les serveurs frontaux (service RTCSERV) dans tous les pools où le mode partage de lignes a été installé et activé :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-117">Restart all the Front End Servers (RTCSRV service) in all the pools where SLA was installed and enabled:</span></span>
        
        ```powershell 
        Stop-CsWindowsService RTCSRV Start-CsWindowsService RTCSRV
                        
        ```

</div>

<div>

## <a name="create-an-sla-group-and-add-users-to-it"></a><span data-ttu-id="bb3d6-118">Créez un groupe de mode partage de lignes et ajoutez-y des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-118">Create an SLA group and add users to it</span></span>

1.  <span data-ttu-id="bb3d6-119">Créez le groupe de mode partage de lignes à l’aide de l’applet de commande [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-119">Create the SLA group by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
                -MaxNumberOfCalls <Number> -BusyOption
                <BusyOnBusy|Voicemail|Forward> [-Target
                <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="bb3d6-p104">L’applet de commande Set-CsSlaConfiguration marque le compte SLAGroup1 de Voix Entreprise en tant qu’entité de mode partage de lignes, et le numéro de SLAGroup1 devient le numéro du groupe de mode partage de lignes. Tous les appels vers SLAGroup1 sonneront chez l’ensemble du groupe de mode partage de lignes.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-p104">The Set-CsSlaConfiguration cmdlet marks the Enterprise Voice account SLAGroup1 as an SLA entity, and the number of SLAGroup1 becomes the number for the SLA group. All calls to SLAGroup1 will ring the entire SLA group.</span></span>
    
    <span data-ttu-id="bb3d6-122">L’exemple ci-dessous crée un groupe de mode partage de lignes pour un utilisateur Voix Entreprise existant, SLAGroup1, et utilise le numéro attribué pour SLAGroup1 comme numéro de ligne principale du mode partage de lignes.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-122">The following example creates an SLA group for an existing Enterprise Voice user, SLAGroup1, and uses the number assigned for SLAGroup1 as the SLA mainline number.</span></span>
    
    <span data-ttu-id="bb3d6-123">La commande définit le nombre maximal d’appels simultanés pour le nouveau groupe de mode partage de lignes sur 3. Les appels qui dépassent cette limitent entendront une tonalité Occupé :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-123">The command sets the maximum number of concurrent calls for the new SLA group to 3, and for calls in excess of that to hear a busy signal:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MaxNumberOfCalls 3
                -BusyOption BusyOnBusy
    ```
    <span data-ttu-id="bb3d6-124">Vous pouvez utiliser Set-CsSlaConfiguration pour créer un groupe de mode partage de lignes ou modifier un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-124">You can use Set-CsSlaConfiguration to create a new SLA group or modify an existing one.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bb3d6-125">Notez que ce que vous spécifiez pour <CODE>-Identity</CODE> doit être un compte d’utilisateur valide pour la voix entreprise valide.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-125">Note that what you specify for <CODE>-Identity</CODE> must be a valid existing Enterprise Voice-enabled user account.</span></span>

    
    </div>

2.  <span data-ttu-id="bb3d6-126">Ajoutez des délégués au groupe à l’aide de l’applet de commande [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-126">Add delegates to the group by using the [Add-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/add-cssladelegates) cmdlet:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="bb3d6-127">L’exemple ci-dessous permet d’ajouter un utilisateur au groupe de mode partage de lignes.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-127">The following example adds a user to the SLA group.</span></span> <span data-ttu-id="bb3d6-128">Chaque utilisateur ajouté au groupe doit être un utilisateur valide d’entreprise Voice :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-128">Each user added to the group must be a valid Enterprise Voice-enabled user:</span></span>
    ```powershell
    Add-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate1@contoso.com
    ```
    <span data-ttu-id="bb3d6-p106">Répétez l’applet de commande pour chaque utilisateur que vous voulez ajouter au groupe. Les utilisateurs peuvent seulement appartenir à un seul groupe de mode de partage de lignes.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-p106">Repeat the cmdlet for each user you want to add to the group. Users can only belong to a single SLA group.</span></span>

</div>

<div>

## <a name="configure-the-sla-group-busy-option"></a><span data-ttu-id="bb3d6-131">Configuration de l’option Occupé du groupe de mode partage de lignes</span><span class="sxs-lookup"><span data-stu-id="bb3d6-131">Configure the SLA group Busy Option</span></span>

1.  <span data-ttu-id="bb3d6-132">Configurez l’option Occupé du groupe de mode partage de lignes à l’aide de l’applet de commande [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-132">Configure the SLA group Busy Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup>
              -BusyOption <Option> [-Target <TargetUserOrPhoneNumber>]
    ```
    <span data-ttu-id="bb3d6-133">L’exemple suivant définit les appels qui dépassent le nombre maximal d’appels simultanés à transférer vers le numéro de téléphone 202-555-1234.</span><span class="sxs-lookup"><span data-stu-id="bb3d6-133">The following example sets calls that exceed the maximum number of concurrent calls to be forwarded to the telephone number 202-555-1234.</span></span> <span data-ttu-id="bb3d6-134">La cible peut être un utilisateur au sein de votre organisation plutôt qu’un numéro de téléphone. dans ce cas, la syntaxe de la personne qui reçoit les appels transférés est la même que lorsque vous spécifiez un délégué : `sip:<NameofDelegate@domain>` .</span><span class="sxs-lookup"><span data-stu-id="bb3d6-134">The target could be a user in your organization instead of a phone number; in that case, the syntax for the person to receive the forwarded calls is the same as when you specify a delegate: `sip:<NameofDelegate@domain>`.</span></span> <span data-ttu-id="bb3d6-135">Le autre paramètre possible pour `BusyOption` est le `Voicemail` suivant :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-135">The other possible parameter for `BusyOption` is `Voicemail`:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -BusyOption Forward
              -Target tel:+2025551234]
    ```
</div>

<div>

## <a name="configure-the-sla-group-missed-call-option"></a><span data-ttu-id="bb3d6-136">Configuration de l’option Appel manqué du groupe de mode partage de lignes</span><span class="sxs-lookup"><span data-stu-id="bb3d6-136">Configure the SLA group Missed Call Option</span></span>

1.  <span data-ttu-id="bb3d6-137">Configurez l’option Appel manqué du groupe de mode partage de lignes à l’aide de l’applet de commande [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-137">Configure the SLA group Missed Call Option by using the [Set-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/set-csslaconfiguration) cmdlet:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity <IdentityOfGroup> 
              -MissedCallOption <Option> -MissedCallForwardTarget
              <TargetUserOrPhoneNumber> -BusyOption <Option> -MaxNumberofCalls <#> -Target [Target]
    ```
    <span data-ttu-id="bb3d6-138">L’exemple suivant spécifie que les appels manqués doivent être renvoyés à l’utilisateur nommé `sla_forward_number` .</span><span class="sxs-lookup"><span data-stu-id="bb3d6-138">The following example specifies that missed calls are to be forwarded to the user named `sla_forward_number`.</span></span> <span data-ttu-id="bb3d6-139">Les options valides pour le `-MissedCallOption` paramètre sont `Forward` , `BusySignal` ou `Disconnect` .</span><span class="sxs-lookup"><span data-stu-id="bb3d6-139">The valid options for the `-MissedCallOption` parameter are `Forward`, `BusySignal`, or `Disconnect`.</span></span> <span data-ttu-id="bb3d6-140">Si vous `Forward` le souhaitez, vous devez également inclure le `-MissedCallForwardTarget` paramètre, avec un utilisateur ou un numéro de téléphone comme destination :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-140">If you choose `Forward`, you must also include the `-MissedCallForwardTarget` parameter, with a user or phone number as the target:</span></span>
    ```powershell
    Set-CsSlaConfiguration -Identity SLAGroup1 -MissedCallOption
              Forward -MissedCallForwardTarget sip:sla_forward_number@contoso.com 
        -BusyOption Forward -MaxNumberOfCalls 2 -Target sip:sla_forward_number@contoso.com 
    ```
</div>

<div>

## <a name="remove-a-delegate-from-a-group"></a><span data-ttu-id="bb3d6-141">Suppression d’un délégué d’un groupe</span><span class="sxs-lookup"><span data-stu-id="bb3d6-141">Remove a delegate from a group</span></span>

1.  <span data-ttu-id="bb3d6-142">Supprimez un délégué d’un groupe à l’aide de l’applet de commande [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-142">Remove a delegate from a group by using the [Remove-CsSlaDelegates](https://docs.microsoft.com/powershell/module/skype/remove-cssladelegates) cmdlet:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity <IdentityOfGroup> -Delegate
              <NameOfDelegate@domain>
    ```
    <span data-ttu-id="bb3d6-143">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-143">For example:</span></span>
    ```powershell
    Remove-CsSlaDelegates -Identity SLAGroup1 -Delegate
              sip:SLA_Delegate3@contoso.com
    ```
</div>

<div>

## <a name="delete-an-sla-group"></a><span data-ttu-id="bb3d6-144">Suppression d’un groupe de mode partage de lignes</span><span class="sxs-lookup"><span data-stu-id="bb3d6-144">Delete an SLA group</span></span>

1.  <span data-ttu-id="bb3d6-145">Supprimez un groupe de mode partage de lignes à l’aide de l’applet de commande [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps) :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-145">Delete an SLA group by using the [Remove-CsSlaConfiguration](https://docs.microsoft.com/powershell/module/skype/remove-csslaconfiguration?view=skype-ps) cmdlet:</span></span>
    
    ```powershell
    Remove-CsSlaConfiguration -Identity <IdentityOfGroup>
              
    ```
    
    <span data-ttu-id="bb3d6-146">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="bb3d6-146">For example:</span></span>
    ```powershell
    Remove-CsSlaConfiguration -Identity SLAGroup1 
    ```
<span data-ttu-id="bb3d6-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb3d6-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

