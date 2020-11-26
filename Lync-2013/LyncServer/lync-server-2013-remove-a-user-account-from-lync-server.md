---
title: 'Lync Server 2013 : supprimer un compte d’utilisateur de Lync Server'
description: 'Lync Server 2013 : supprimer un compte d’utilisateur de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove a user account from Lync Server
ms:assetid: 2f512aba-e358-45ae-af58-74312ee9c514
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688008(v=OCS.15)
ms:contentKeyID: 49733596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201eb8a7ba620792b92e2c7983890047c249ce86
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436446"
---
# <a name="remove-a-user-account-from-lync-server-2013"></a><span data-ttu-id="c4f98-103">Supprimer un compte d’utilisateur de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4f98-103">Remove a user account from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4f98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4f98-104">

<span> </span></span></span>

<span data-ttu-id="c4f98-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="c4f98-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="c4f98-106">Vous pouvez utiliser la procédure suivante pour supprimer un compte d’utilisateur déjà ajouté dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c4f98-106">You can use the following procedure to remove a previously added user account in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c4f98-107">La suppression d’un utilisateur entraîne la perte des paramètres que vous avez configurés pour le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4f98-107">Removing a user will cause you to lose any settings you configured for the user account.</span></span> <span data-ttu-id="c4f98-108">Si vous voulez désactiver temporairement un compte d’utilisateur à la place, reportez-vous à la rubrique <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">désactiver ou réactiver un compte d’utilisateur pour Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c4f98-108">If you would like to temporarily disable a user account instead, see the topic <A href="lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md">Disable or re-enable user account for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-remove-a-user-account-by-using-lync-server-management-shell"></a><span data-ttu-id="c4f98-109">Pour supprimer un compte d’utilisateur à l’aide de Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="c4f98-109">To remove a user account by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="c4f98-110">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="c4f98-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="c4f98-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c4f98-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="c4f98-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="c4f98-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="c4f98-113">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="c4f98-113">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="c4f98-114">Dans la boîte de dialogue **Rechercher des utilisateurs** , tapez tout ou la première partie du nom complet, prénom, nom, nom du compte de comptes de sécurité (Sam), adresse SIP ou URI (Uniform Resource Identifier) du compte d’utilisateur que vous souhaitez désactiver ou réactiver, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="c4f98-114">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to disable or re-enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="c4f98-115">Dans la table, cliquez sur le compte d’utilisateur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="c4f98-115">In the table, click the user account that you want to remove.</span></span>

6.  <span data-ttu-id="c4f98-116">Dans le menu **action** , sélectionnez **supprimer de Lync Server** et une boîte de dialogue s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c4f98-116">On the **Action** menu, select **Remove from Lync Server**, and a dialog box appears.</span></span>

7.  <span data-ttu-id="c4f98-117">Dans la boîte de dialogue, sélectionnez **OK** pour supprimer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4f98-117">From the dialog box, select **OK** to remove the user.</span></span>

</div>

<div>

## <a name="removing-user-accounts-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="c4f98-118">Suppression de comptes d’utilisateur à l’aide des applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4f98-118">Removing User Accounts by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="c4f98-119">Vous pouvez supprimer des comptes d’utilisateurs à l’aide de l’applet de dialogue Disable-CsUser.</span><span class="sxs-lookup"><span data-stu-id="c4f98-119">You can remove user accounts by using the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="c4f98-120">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4f98-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="c4f98-121">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="c4f98-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-user-account"></a><span data-ttu-id="c4f98-122">Pour supprimer un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="c4f98-122">To remove a user account</span></span>

  - <span data-ttu-id="c4f98-123">Pour supprimer un compte d’utilisateur, utilisez l’applet de Disable-CsUser cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f98-123">To remove a user account, use the Disable-CsUser cmdlet.</span></span> <span data-ttu-id="c4f98-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c4f98-124">For example:</span></span>
    
        Disable-CsUser -Identity "Ken Myer"
    
    <span data-ttu-id="c4f98-125">Après avoir exécuté cette commande, il est impossible de réactiver le compte et ses paramètres précédents.</span><span class="sxs-lookup"><span data-stu-id="c4f98-125">After this command has run there is no way to re-enable the account and its previous settings.</span></span> <span data-ttu-id="c4f98-126">À la place, vous devez utiliser l’applet de applet de Enable-CsUser pour créer un compte de marque pour Ken Myer.</span><span class="sxs-lookup"><span data-stu-id="c4f98-126">Instead, you will need to use the Enable-CsUser cmdlet to create a brand-new account for Ken Myer.</span></span>

</div>

<span data-ttu-id="c4f98-127">Pour plus d’informations, reportez-vous à la rubrique d’aide de l’applet de la cmdlet [Disable-Csuser](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="c4f98-127">For more information, see the help topic for the [Disable-CsUser](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c4f98-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4f98-128">See Also</span></span>


[<span data-ttu-id="c4f98-129">Désactiver ou réactiver le compte d’utilisateur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4f98-129">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  


[<span data-ttu-id="c4f98-130">Activation et désactivation des utilisateurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4f98-130">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="c4f98-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4f98-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

