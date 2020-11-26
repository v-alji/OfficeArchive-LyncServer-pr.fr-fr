---
title: 'Lync Server 2013 : désactiver ou réactiver un compte d’utilisateur pour Lync Server'
description: 'Lync Server 2013 : désactiver ou réactiver le compte d’utilisateur de Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable or re-enable user account for Lync Server
ms:assetid: 12497d00-f665-4a97-be68-854c5a8be4fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429696(v=OCS.15)
ms:contentKeyID: 48183455
ms.date: 04/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b30d83d7a7f38b84f8e669ac06947eebf4a8545
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437839"
---
# <a name="disable-or-re-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="93017-103">Désactiver ou réactiver le compte d’utilisateur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93017-103">Disable or re-enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93017-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93017-104">

<span> </span></span></span>

<span data-ttu-id="93017-105">_**Dernière modification de la rubrique :** 2016-04-04_</span><span class="sxs-lookup"><span data-stu-id="93017-105">_**Topic Last Modified:** 2016-04-04_</span></span>

<span data-ttu-id="93017-106">Vous pouvez utiliser la procédure suivante pour désactiver un compte d’utilisateur déjà activé dans Lync Server 2013 sans perdre les paramètres de serveur Lync que vous avez configurés pour le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93017-106">You can use the following procedure to disable a previously enabled user account in Lync Server 2013 without losing the Lync Server settings that you configured for the user account.</span></span> <span data-ttu-id="93017-107">Étant donné que vous ne perdez pas les paramètres de compte d’utilisateur de Lync Server, vous pouvez réactiver un compte d’utilisateur déjà activé sans avoir à reconfigurer le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93017-107">Because you do not lose the Lync Server user account settings, you can re-enable a previously enabled user account again without having to reconfigure the user account.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="93017-108">La désactivation d’un compte d’utilisateur dans Active Directory n' <STRONG>empêchera pas</STRONG> un utilisateur de se connecter ou d’utiliser Lync Server.</span><span class="sxs-lookup"><span data-stu-id="93017-108">Simply disabling a user account in Active Directory <STRONG>will not</STRONG> stop a user from being able to sign into or use Lync Server.</span></span> <span data-ttu-id="93017-109">En effet, Lync utilise l’authentification par certificat qui rationalise le processus d’authentification, et ces certificats clients sont valides pour 180 jours.</span><span class="sxs-lookup"><span data-stu-id="93017-109">This is because Lync uses certificate authentication that streamlines the authentication process, and these client certificates are valid for 180 days.</span></span> <span data-ttu-id="93017-110">Si vous souhaitez désactiver les comptes Active Directory désactivés qui ont été activés pour Lync et avoir accès à Lync Server, vous devez utiliser l’applet de commande <STRONG>Disable-Csuser</STRONG> , ou utiliser le <STRONG>panneau de configuration de Lync Server</STRONG> comme prévu dans cet article.</span><span class="sxs-lookup"><span data-stu-id="93017-110">If you want to stop disabled Active Directory accounts that had been enabled for Lync from having access to Lync Server, you must use the <STRONG>Disable-CsUser</STRONG> cmdlet, or use the <STRONG>Lync Server Control Panel</STRONG> as laid out in this article.</span></span> <span data-ttu-id="93017-111">Lorsque l’utilisateur est désactivé dans Lync et que le magasin de gestion central a été répliqué dans l’environnement, les utilisateurs ne seront plus en mesure de se connecter.</span><span class="sxs-lookup"><span data-stu-id="93017-111">Once the user is disabled in Lync and the Central Management store has been replicated in the environment the users will no longer be able to sign in.</span></span> <span data-ttu-id="93017-112">De plus, les utilisateurs connectés seront déconnectés.</span><span class="sxs-lookup"><span data-stu-id="93017-112">Also, users that are signed in will get disconnected.</span></span>



</div>

<div>

## <a name="to-disable-or-re-enable-a-previously-enabled-user-account-for-lync-server"></a><span data-ttu-id="93017-113">Pour désactiver ou réactiver un compte d’utilisateur déjà activé pour Lync Server</span><span class="sxs-lookup"><span data-stu-id="93017-113">To disable or re-enable a previously enabled user account for Lync Server</span></span>

1.  <span data-ttu-id="93017-114">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="93017-114">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="93017-115">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="93017-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="93017-116">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="93017-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="93017-117">Dans la barre de navigation de gauche, cliquez sur **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="93017-117">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="93017-118">Dans la boîte de dialogue **Rechercher des utilisateurs** , tapez tout ou la première partie du nom complet, prénom, nom, nom du compte de comptes de sécurité (Sam), adresse SIP ou URI (Uniform Resource Identifier) du compte d’utilisateur que vous souhaitez désactiver ou réactiver, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="93017-118">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to disable or re-enable, and then click **Find**.</span></span>

5.  <span data-ttu-id="93017-119">Dans la table, cliquez sur le compte d’utilisateur que vous souhaitez désactiver ou réactiver.</span><span class="sxs-lookup"><span data-stu-id="93017-119">In the table, click the user account that you want to disable or re-enable.</span></span>

6.  <span data-ttu-id="93017-120">Dans le menu **action** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="93017-120">On the **Action** menu, do one of the following:</span></span>
    
      - <span data-ttu-id="93017-121">Pour désactiver temporairement le compte d’utilisateur pour Lync Server 2013, cliquez sur **désactiver temporairement pour Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="93017-121">To temporarily disable the user account for Lync Server 2013, click **Temporarily disable for Lync Server**.</span></span>
    
      - <span data-ttu-id="93017-122">Pour activer le compte d’utilisateur pour Lync Server 2013, cliquez sur **réactiver pour Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="93017-122">To enable the user account for Lync Server 2013, click **Re-enable for Lync Server**.</span></span>

</div>

<div>

## <a name="using-windows-powershell-to-disable-or-re-enable-user-accounts"></a><span data-ttu-id="93017-123">Utilisation de Windows PowerShell pour désactiver ou réactiver les comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="93017-123">Using Windows PowerShell to Disable or Re-enable User Accounts</span></span>

<span data-ttu-id="93017-124">Pour désactiver temporairement les comptes d’utilisateurs, vous pouvez les réactiver ultérieurement à l’aide de l’applet de dialogue **Set-Csuser** .</span><span class="sxs-lookup"><span data-stu-id="93017-124">User accounts can be temporarily disabled, and then later re-enabled, by using the **Set-CsUser** cmdlet.</span></span> <span data-ttu-id="93017-125">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93017-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="93017-126">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="93017-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-disable-a-user-account"></a><span data-ttu-id="93017-127">Pour désactiver un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="93017-127">To disable a user account</span></span>

  - <span data-ttu-id="93017-128">Pour désactiver temporairement un compte d’utilisateur, définissez la valeur de la propriété Enabled sur false ($False).</span><span class="sxs-lookup"><span data-stu-id="93017-128">To temporarily disable a user account, set the value of the Enabled property to False ($False).</span></span> <span data-ttu-id="93017-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="93017-129">For example:</span></span>
    
        Set-CsUser -Identity "Ken Myer" -Enabled $False

</div>

<div>

## <a name="to-re-enable-a-user-account"></a><span data-ttu-id="93017-130">Pour réactiver un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="93017-130">To re-enable a user account</span></span>

  - <span data-ttu-id="93017-131">Pour réactiver un compte d’utilisateur désactivé, définissez la valeur de la propriété Enabled sur true ($True).</span><span class="sxs-lookup"><span data-stu-id="93017-131">To re-enable a disabled user account, set the value of the Enabled property to True ($True).</span></span> <span data-ttu-id="93017-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="93017-132">For example:</span></span>
    
        Set-CsUser -Identity "Ken Myer" -Enabled $True

</div>

<span data-ttu-id="93017-133">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-Csuser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) .</span><span class="sxs-lookup"><span data-stu-id="93017-133">For more information, see the help topic for the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="93017-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93017-134">See Also</span></span>


[<span data-ttu-id="93017-135">Ajouter et activer un compte d’utilisateur pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93017-135">Add and enable user account for Lync Server 2013</span></span>](lync-server-2013-add-and-enable-user-account-for-lync-server.md)  


[<span data-ttu-id="93017-136">Activation et désactivation des utilisateurs pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93017-136">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="93017-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93017-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

