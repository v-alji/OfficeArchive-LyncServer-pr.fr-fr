---
title: 'Lync Server 2013 : activation ou désactivation des notifications de transmission pour les iPhone'
description: 'Lync Server 2013 : activation ou désactivation des notifications de transmission pour les iPhone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling push notifications for iPhones
ms:assetid: 8bbf531a-807f-4a8f-814a-94bfed8f97ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688122(v=OCS.15)
ms:contentKeyID: 49733719
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07a9c5ec442c3628455797b987d8b2f22677e70e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394701"
---
# <a name="enabling-or-disabling-push-notifications-for-iphones-in-lync-server-2013"></a><span data-ttu-id="85dd9-103">Activation ou désactivation des notifications de transmission pour les iPhone dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85dd9-103">Enabling or disabling push notifications for iPhones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85dd9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85dd9-104">

<span> </span></span></span>

<span data-ttu-id="85dd9-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="85dd9-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="85dd9-106">Les notifications de transmission sous forme de badges, d’icônes ou d’alertes peuvent être envoyées à un iPhone même lorsque l’application mobile n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="85dd9-106">Push notifications, in the form of badges, icons, or alerts, can be sent to an iPhone even when the mobile application is inactive.</span></span> <span data-ttu-id="85dd9-107">Les notifications de transmission avertissent un utilisateur d’événements tels qu’une invitation à la messagerie instantanée, une invitation à une nouvelle ou une messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="85dd9-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="85dd9-108">Vous pouvez activer ou désactiver les notifications de transmission pour iPhone à l’aide de Lync Server 2013 Control Panel ou de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="85dd9-108">You can enable or disable push notifications for iPhone by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-enable-push-notifications-for-iphone-by-using-lync-server-control-panel"></a><span data-ttu-id="85dd9-109">Pour activer les notifications de transmission pour iPhone en utilisant le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="85dd9-109">To enable push notifications for iPhone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="85dd9-110">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="85dd9-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="85dd9-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85dd9-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="85dd9-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="85dd9-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="85dd9-113">Dans la barre de navigation gauche, cliquez sur **clients**, puis sur le bouton de navigation **configuration de notifications de transmission** .</span><span class="sxs-lookup"><span data-stu-id="85dd9-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="85dd9-114">Dans la page **configuration de notifications de transmission** , cliquez sur le site que vous voulez modifier, cliquez sur le menu **modifier** , puis cliquez sur Afficher les **Détails**.</span><span class="sxs-lookup"><span data-stu-id="85dd9-114">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="85dd9-115">Activez la case à cocher **activer les notifications de type Apple** .</span><span class="sxs-lookup"><span data-stu-id="85dd9-115">Click the **Enable Apple push notifications** checkbox.</span></span>

6.  <span data-ttu-id="85dd9-116">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="85dd9-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-push-notifications-for-iphone-by-using-lync-server-control-panel"></a><span data-ttu-id="85dd9-117">Pour désactiver les notifications de transmission pour iPhone en utilisant le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="85dd9-117">To disable push notifications for iPhone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="85dd9-118">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="85dd9-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="85dd9-119">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="85dd9-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="85dd9-120">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="85dd9-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="85dd9-121">Dans la barre de navigation gauche, cliquez sur **clients**, puis sur le bouton de navigation **configuration de notifications de transmission** .</span><span class="sxs-lookup"><span data-stu-id="85dd9-121">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="85dd9-122">Dans la page **configuration de notifications de transmission** , cliquez sur le site que vous voulez modifier, cliquez sur le menu **modifier** , puis cliquez sur Afficher les **Détails**.</span><span class="sxs-lookup"><span data-stu-id="85dd9-122">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="85dd9-123">Décochez la case **activer les notifications de type Apple** .</span><span class="sxs-lookup"><span data-stu-id="85dd9-123">Clear the **Enable Apple push notifications** checkbox.</span></span>

6.  <span data-ttu-id="85dd9-124">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="85dd9-124">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-push-notifications-to-iphone-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="85dd9-125">Activation ou désactivation des notifications de transmission pour iPhone à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="85dd9-125">Enabling or Disabling Push Notifications to iPhone by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="85dd9-126">Les notifications de transmission vers Apple iPhone peuvent être activées ou désactivées à l’aide de l’applet de cmdlet **Set-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="85dd9-126">Push notifications to Apple iPhone can be enabled or disabled by using the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="85dd9-127">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85dd9-127">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="85dd9-128">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="85dd9-128">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-push-notifications-for-iphone"></a><span data-ttu-id="85dd9-129">Pour activer les notifications de transmission pour iPhone</span><span class="sxs-lookup"><span data-stu-id="85dd9-129">To enable push notifications for iPhone</span></span>

  - <span data-ttu-id="85dd9-130">Pour activer les notifications de transmission pour iPhone, définissez la valeur de la propriété EnableApplePushNotificationService sur true ($True).</span><span class="sxs-lookup"><span data-stu-id="85dd9-130">To enable push notifications for iPhone set the value of the EnableApplePushNotificationService property to True ($True).</span></span> <span data-ttu-id="85dd9-131">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="85dd9-131">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableApplePushNotificationService $True

</div>

<div>

## <a name="to-disable-push-notifications-for-iphone"></a><span data-ttu-id="85dd9-132">Pour désactiver les notifications de transmission pour iPhone</span><span class="sxs-lookup"><span data-stu-id="85dd9-132">To disable push notifications for iPhone</span></span>

  - <span data-ttu-id="85dd9-133">Pour désactiver les notifications de transmission pour iPhone, définissez la valeur de la propriété EnableApplePushNotificationService sur false ($False).</span><span class="sxs-lookup"><span data-stu-id="85dd9-133">To disable push notifications for iPhone set the value of the EnableApplePushNotificationService property to False ($False).</span></span> <span data-ttu-id="85dd9-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="85dd9-134">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableApplePushNotificationService $False

</div>

<span data-ttu-id="85dd9-135">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de passe [Set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="85dd9-135">For more information, see the help topic for the [Set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85dd9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85dd9-136">See Also</span></span>


[<span data-ttu-id="85dd9-137">Configuration des notifications push dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85dd9-137">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="85dd9-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85dd9-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

