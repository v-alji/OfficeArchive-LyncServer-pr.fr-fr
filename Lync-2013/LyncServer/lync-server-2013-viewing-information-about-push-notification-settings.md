---
title: 'Lync Server 2013 : affichage d’informations sur les paramètres de notifications de transmission'
description: 'Lync Server 2013 : affichage d’informations sur les paramètres de notifications de transmission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing information about push notification settings
ms:assetid: be5c6b01-4294-4d17-9772-fed40201e8a5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721868(v=OCS.15)
ms:contentKeyID: 49733801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44ee876df341833c93e97fd16664940629754a6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443978"
---
# <a name="viewing-information-about-push-notification-settings-in-lync-server-2013"></a><span data-ttu-id="319ea-103">Affichage d’informations sur les paramètres de notifications de transmission dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="319ea-103">Viewing information about push notification settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="319ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="319ea-104">

<span> </span></span></span>

<span data-ttu-id="319ea-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="319ea-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="319ea-106">Les notifications de transmission sous forme de badges, d’icônes ou d’alertes peuvent être envoyées à un appareil mobile même lorsque l’application mobile n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="319ea-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="319ea-107">Les notifications de transmission avertissent un utilisateur d’événements tels qu’une invitation à la messagerie instantanée, une invitation à une nouvelle ou une messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="319ea-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="319ea-108">Vous pouvez afficher les paramètres de notifications de transmission des informations pour les appareils mobiles à l’aide de Lync Server 2013 Control Panel ou de Lync Server 2013 Management Shell.</span><span class="sxs-lookup"><span data-stu-id="319ea-108">You can view information push notifications settings for mobile devices by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-view-push-notification-information-from-lync-server-control-panel"></a><span data-ttu-id="319ea-109">Pour afficher les informations de notifications de transmission depuis le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="319ea-109">To view push notification information from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="319ea-110">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="319ea-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="319ea-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="319ea-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="319ea-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="319ea-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="319ea-113">Dans la barre de navigation gauche, cliquez sur **clients**, puis sur le bouton de navigation **configuration de notifications de transmission** .</span><span class="sxs-lookup"><span data-stu-id="319ea-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="319ea-114">Dans la page **configuration de notifications de transmission** , cliquez sur le site que vous souhaitez afficher, cliquez sur le menu **modifier** , puis cliquez sur Afficher les **Détails**.</span><span class="sxs-lookup"><span data-stu-id="319ea-114">On the **Push Notification Configuration** page, click the site you want to view, click the **Edit** menu, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-push-notification-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="319ea-115">Affichage des informations de notifications de transmission à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="319ea-115">Viewing Push Notification Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="319ea-116">Vous pouvez afficher les paramètres de configuration de la notification de transmission à l’aide de Windows PowerShell et de l’applet **de cmdlet Get-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="319ea-116">You can view push notification configuration settings by using Windows PowerShell and the **Get-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="319ea-117">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="319ea-117">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="319ea-118">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="319ea-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-push-notification-configuration-information"></a><span data-ttu-id="319ea-119">Pour afficher les informations de configuration des notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="319ea-119">To view push notification configuration information</span></span>

  - <span data-ttu-id="319ea-120">Pour afficher des informations sur les paramètres de configuration de votre notification d’émission, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="319ea-120">To view information about all your push notification configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsPushNotificationConfiguration
    
    <span data-ttu-id="319ea-121">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="319ea-121">That will return information similar to this:</span></span>
    
        Identity                               : Global
        EnableApplePushNotificationService     : False
        EnableMicrosoftPushNotificationService : False

</div>

<span data-ttu-id="319ea-122">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="319ea-122">For more information, see the help topic for the [Get-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="319ea-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="319ea-123">See Also</span></span>


[<span data-ttu-id="319ea-124">Configuration des notifications push dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="319ea-124">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="319ea-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="319ea-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

