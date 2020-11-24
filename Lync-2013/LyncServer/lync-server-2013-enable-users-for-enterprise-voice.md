---
title: 'Lync Server 2013 : activer les utilisateurs pour voix entreprise'
description: 'Lync Server 2013 : activez les utilisateurs pour voix entreprise.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for Enterprise Voice
ms:assetid: f252b23b-9641-4160-aa81-bf06dc2eced3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413011(v=OCS.15)
ms:contentKeyID: 48185800
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8aa8dbbeb507ced5217e517c1608c3a2a9259668
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395209"
---
# <a name="enable-users-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="5da05-103">Activer les utilisateurs d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5da05-103">Enable users for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5da05-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5da05-104">

<span> </span></span></span>

<span data-ttu-id="5da05-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5da05-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5da05-106">Après avoir installé les fichiers pour un ou plusieurs serveurs de médiation, configuré le routage des appels sortants et éventuellement une ou plusieurs fonctionnalités avancées de voix entreprise, vous pouvez utiliser les procédures suivantes pour permettre à un utilisateur d’effectuer des appels à l’aide d’Enterprise Voice :</span><span class="sxs-lookup"><span data-stu-id="5da05-106">After you install files for one or more Mediation Servers, configure outbound call routing, and optionally deploy one or more advanced Enterprise Voice features, you can use the following procedures to enable a user to make calls by using Enterprise Voice:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5da05-107">Parmi les procédures ci-dessous, seules les premières peuvent être effectuées à l’aide du panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5da05-107">Of the following procedures, only the first can be performed by using Lync Server Control Panel.</span></span> <span data-ttu-id="5da05-108">Pour les procédures restantes, vous pouvez uniquement utiliser Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="5da05-108">For the remaining procedures, you can use only Lync Server Management Shell.</span></span>



</div>

  - <span data-ttu-id="5da05-109">Activez le compte d’utilisateur voix entreprise voix.</span><span class="sxs-lookup"><span data-stu-id="5da05-109">Enable the user account for Enterprise Voice.</span></span>

  - <span data-ttu-id="5da05-110">(Facultatif) Affectez au compte d’utilisateur une stratégie de voix spécifique à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5da05-110">(Optional) Assign the user account a user-specific voice policy.</span></span>

  - <span data-ttu-id="5da05-111">(Facultatif) Affectez au compte d’utilisateur un plan de numérotation spécifique à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5da05-111">(Optional) Assign the user account a user-specific dial plan.</span></span>

<div>

## <a name="to-enable-a-user-account-for-enterprise-voice"></a><span data-ttu-id="5da05-112">Pour activer un compte d’utilisateur pour voix entreprise</span><span class="sxs-lookup"><span data-stu-id="5da05-112">To enable a user account for Enterprise Voice</span></span>

1.  <span data-ttu-id="5da05-113">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="5da05-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5da05-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5da05-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5da05-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5da05-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5da05-116">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="5da05-116">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="5da05-117">Dans la zone **Rechercher des utilisateurs**, tapez le début ou l’intégralité du nom d’affichage, du prénom, du nom de famille, du nom de compte SAM (Security Accounts Manager), de l’adresse SIP (Session Initiation Protocol) ou de l’URI de ligne du compte d’utilisateur à activer, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="5da05-117">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="5da05-118">Dans la table, cliquez sur le compte d’utilisateur que vous souhaitez activer pour voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="5da05-118">In the table, click the user account that you want to enable for Enterprise Voice.</span></span>

6.  <span data-ttu-id="5da05-119">Dans le menu **Edition**, cliquez sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="5da05-119">On the **Edit** menu, click **Show details**.</span></span>

7.  <span data-ttu-id="5da05-120">Dans la page **modifier l’utilisateur de Lync Server** , sous **téléphonie**, cliquez sur **voix entreprise**.</span><span class="sxs-lookup"><span data-stu-id="5da05-120">On the **Edit Lync Server User** page, under **Telephony**, click **Enterprise Voice**.</span></span>

8.  <span data-ttu-id="5da05-121">Cliquez sur **URI de ligne**, puis tapez un numéro de téléphone normalisé unique (par exemple, tél :+14255550200).</span><span class="sxs-lookup"><span data-stu-id="5da05-121">Click **Line URI**, and then type a unique, normalized phone number (for example, tel:+14255550200).</span></span>

9.  <span data-ttu-id="5da05-122">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="5da05-122">Click **Commit**.</span></span>

<span data-ttu-id="5da05-123">Pour terminer l’activation d’un utilisateur pour voix entreprise, assurez-vous que l’utilisateur dispose d’une stratégie vocale et d’un plan de numérotation, qu’il s’agisse de global (attribué par défaut) ou d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5da05-123">To finish enabling a user for Enterprise Voice, be sure that the user is assigned a voice policy and a dial plan, whether global (assigned by default) or user-specific.</span></span>

<span data-ttu-id="5da05-124">Par défaut, tous les utilisateurs se voient affecter une stratégie de voix et un plan de numérotation d’ordre global.</span><span class="sxs-lookup"><span data-stu-id="5da05-124">By default, all users are assigned a global voice policy and dial plan.</span></span> <span data-ttu-id="5da05-125">S’il existe une stratégie de voix ou un plan de numérotation au niveau du site sur lequel un compte d’utilisateur est hébergé, cette stratégie de site s’applique automatiquement à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5da05-125">If a voice policy or dial plan exists at the site level for the site on which the user account is homed, those site policies will automatically apply to the user.</span></span> <span data-ttu-id="5da05-126">Pour appliquer une stratégie de voix ou un plan de numérotation à un utilisateur, vous devez exécuter les applets de commande **Grant-CsVoicePolicy** et **Grant-CsDialPlan**.</span><span class="sxs-lookup"><span data-stu-id="5da05-126">To apply a per-user voice policy or dial plan to a user, you must run the **Grant-CsVoicePolicy** and **Grant-CsDialPlan** cmdlets.</span></span> <span data-ttu-id="5da05-127">Pour plus d’informations, consultez la documentation de [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5da05-127">For details, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

<div>

## <a name="voice-policy-assignment"></a><span data-ttu-id="5da05-128">Affectation d’une stratégie de voix</span><span class="sxs-lookup"><span data-stu-id="5da05-128">Voice Policy Assignment</span></span>

<span data-ttu-id="5da05-129">Les stratégies de voix globale et de niveau site sont automatiquement affectées à tous les comptes d’utilisateurs activés pour Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="5da05-129">Global and site-level voice policies are automatically assigned to all user accounts that are enabled for Enterprise Voice.</span></span> <span data-ttu-id="5da05-130">Vous pouvez également créer des stratégies de voix qui s’appliquent à des utilisateurs ou à des groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5da05-130">You can also create voice policies that apply to specific users or groups.</span></span> <span data-ttu-id="5da05-131">Ces stratégies utilisateur doivent être affectées explicitement à des utilisateurs ou à des groupes.</span><span class="sxs-lookup"><span data-stu-id="5da05-131">These per-user policies must be explicitly assigned to the users or groups.</span></span> <span data-ttu-id="5da05-132">Si vous souhaitez utiliser la politique globale ou vocale pour tous les utilisateurs qui sont activés pour voix entreprise, vous pouvez ignorer cette section et poursuivre la section affectation de plan de numérotation plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5da05-132">If you want to use the global or site voice policy for all users who are enabled for Enterprise Voice, you can skip this section and continue to Dial Plan Assignment section later in this topic.</span></span>

<div>

## <a name="to-assign-a-user-specific-voice-policy"></a><span data-ttu-id="5da05-133">Pour affecter une stratégie de voix spécifique à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5da05-133">To assign a user-specific voice policy</span></span>

1.  <span data-ttu-id="5da05-134">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="5da05-134">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5da05-135">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="5da05-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="5da05-136">Pour affecter une stratégie de voix utilisateur existante à un utilisateur, exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="5da05-136">To assign an existing user voice policy to a user, run the following at the command prompt:</span></span>
    
        Grant-CsVoicePolicy -Identity <UserIdParameter> -PolicyName <String>
    
    <span data-ttu-id="5da05-137">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5da05-137">For example:</span></span>
    
        Grant-CsVoicePolicy -Identity "Bob Kelly" -PolicyName VoicePolicyJapan
    
    <span data-ttu-id="5da05-138">Dans cet exemple, l’utilisateur portant le nom d’affichage Bob Kelly reçoit la politique vocale portant le nom **VoicePolicyJapan**.</span><span class="sxs-lookup"><span data-stu-id="5da05-138">In this example, the user with the display name Bob Kelly is assigned the voice policy with the name **VoicePolicyJapan**.</span></span>

<span data-ttu-id="5da05-139">Pour plus d’informations sur l’attribution d’une stratégie vocale spécifique à un utilisateur ou sur l’exécution de l’applet de connexion **Grant-CsVoicePolicy** , voir la documentation de [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5da05-139">For details about assigning a user-specific voice policy or about running the **Grant-CsVoicePolicy** cmdlet, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

</div>

<span id="BKMK_DialPlanAssignment"></span>

<div>

## <a name="dial-plan-assignment"></a><span data-ttu-id="5da05-140">Affectation d’un plan de numérotation</span><span class="sxs-lookup"><span data-stu-id="5da05-140">Dial Plan Assignment</span></span>

<span data-ttu-id="5da05-141">Pour achever la configuration de compte d’utilisateur pour les utilisateurs d’Enterprise Voice ou les utilisateurs de conférences rendez-vous, l’utilisateur doit être affecté d’un plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="5da05-141">To complete user account configuration for either users of Enterprise Voice or users of dial-in conferencing, the user must be assigned a dial plan.</span></span> <span data-ttu-id="5da05-142">Les comptes d’utilisateurs utilisent automatiquement le plan de numérotation global ou, le cas échéant, le plan de numérotation au niveau du site si vous n’affectez pas explicitement un plan de numérotation utilisateur existant.</span><span class="sxs-lookup"><span data-stu-id="5da05-142">User accounts will automatically use the global dial plan or, if one exists, the site-level dial plan, when you do not explicitly assign an existing per-user dial plan.</span></span> <span data-ttu-id="5da05-143">Si vous souhaitez utiliser le plan de numérotation global ou de numérotation de site pour tous les utilisateurs qui sont activés pour voix entreprise, vous pouvez ignorer cette section.</span><span class="sxs-lookup"><span data-stu-id="5da05-143">If you want to use the global or site dial plan for all users who are enabled for Enterprise Voice, you can skip this section.</span></span>

<div>

## <a name="to-assign-a-dial-plan"></a><span data-ttu-id="5da05-144">Pour affecter un plan de numérotation</span><span class="sxs-lookup"><span data-stu-id="5da05-144">To assign a dial plan</span></span>

1.  <span data-ttu-id="5da05-145">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="5da05-145">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5da05-146">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="5da05-146">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="5da05-147">Pour affecter un plan de numérotation spécifique à un utilisateur, exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="5da05-147">To assign a user-specific dial plan, run the following at the command prompt:</span></span>
    
        Grant-CsDialPlan -Identity <UserIdParameter> -PolicyName <String>
    
    <span data-ttu-id="5da05-148">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5da05-148">For example:</span></span>
    
        Grant-CsDialPlan -Identity "Bob Kelly" -PolicyName DialPlanJapan
    
    <span data-ttu-id="5da05-149">Dans cet exemple, l’utilisateur portant le nom d’affichage Bob Kelly reçoit le plan de numérotation de l’utilisateur portant le nom **DialPlanJapan**.</span><span class="sxs-lookup"><span data-stu-id="5da05-149">In this example, the user with the display name Bob Kelly is assigned the user dial plan with the name **DialPlanJapan**.</span></span>

<span data-ttu-id="5da05-150">Pour plus d’informations sur l’attribution d’un plan de numérotation utilisateur ou sur l’exécution de l’applet de connexion **Grant-CsDialPlan** , voir la documentation de [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5da05-150">For details about assigning a user dial plan or about running the **Grant-CsDialPlan** cmdlet, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5da05-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5da05-151">See Also</span></span>


[<span data-ttu-id="5da05-152">Désactiver un utilisateur pour voix entreprise dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5da05-152">Disable a user for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-disable-a-user-for-enterprise-voice.md)  
  

<span data-ttu-id="5da05-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5da05-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

