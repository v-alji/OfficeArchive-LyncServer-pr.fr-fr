---
title: 'Lync Server 2013 : Configuration des notifications push'
description: 'Lync Server 2013 : configuration pour les notifications de transmission.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring for push notifications
ms:assetid: d77f2c06-0fe6-45d5-8f08-808ab871b3e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690047(v=OCS.15)
ms:contentKeyID: 48185574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24c22ff42f666add9eac4966134c88b9bf680046
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433081"
---
# <a name="configuring-for-push-notifications-in-lync-server-2013"></a><span data-ttu-id="13c24-103">Configuration des notifications push dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13c24-103">Configuring for push notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13c24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13c24-104">

<span> </span></span></span>

<span data-ttu-id="13c24-105">_**Dernière modification de la rubrique :** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="13c24-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<span data-ttu-id="13c24-106">Les notifications de transmission sous forme de badges, d’icônes ou d’alertes peuvent être envoyées à un appareil mobile même lorsque l’application mobile n’est pas active.</span><span class="sxs-lookup"><span data-stu-id="13c24-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="13c24-107">Les notifications de transmission avertissent un utilisateur d’événements tels qu’une invitation à la messagerie instantanée, une invitation à une nouvelle ou une messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="13c24-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="13c24-108">Le service de mobilité Lync Server 2013 envoie les notifications au service de notifications de transmission Lync Server via le Cloud, qui envoie ensuite les notifications au service de notifications de transmission d’Apple (APNS) (pour un appareil Apple exécutant le client mobile Lync 2010) ou le service de notifications par Microsoft (MPNS) (pour un appareil Windows Phone exécutant le client mobile Lync 2013 2010</span><span class="sxs-lookup"><span data-stu-id="13c24-108">The Lync Server 2013 Mobility Service sends the notifications to the cloud-based Lync Server Push Notification Service, which then sends the notifications to the Apple Push Notification Service (APNS) (for an Apple device running the Lync 2010 Mobile client) or the Microsoft Push Notification Service (MPNS) (for a Windows Phone device running the Lync 2010 Mobile or the Lync 2013 Mobile client).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="13c24-109">Si vous utilisez un téléphone Windows Phone avec Lync 2010 mobile ou Lync 2013 mobile, la notification de transmission est une considération importante.</span><span class="sxs-lookup"><span data-stu-id="13c24-109">If you use Windows Phone with Lync 2010 Mobile or Lync 2013 Mobile client, push notification is an important consideration.</span></span><BR><span data-ttu-id="13c24-110">Si vous utilisez Lync 2010 mobile sur des appareils Apple, vous devez tenir compte des notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-110">If you use Lync 2010 Mobile on Apple devices, push notification is an important consideration.</span></span><BR><span data-ttu-id="13c24-111">Si vous utilisez Lync 2013 mobile sur des appareils Apple, vous n’avez plus besoin d’une notification de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-111">If you use Lync 2013 Mobile on Apple devices, you no longer need push notification.</span></span>



</div>

<span data-ttu-id="13c24-112">Configurez votre topologie pour prendre en charge les notifications de transmission en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="13c24-112">Configure your topology to support push notifications by doing the following:</span></span>

  - <span data-ttu-id="13c24-113">Si votre environnement possède un serveur Edge Lync Server 2010 ou Lync Server 2013, vous devez ajouter un nouveau fournisseur d’hébergement, Microsoft Lync Online, puis configurer la Fédération des fournisseurs d’hébergement entre votre organisation et Lync Online.</span><span class="sxs-lookup"><span data-stu-id="13c24-113">If your environment has a Lync Server 2010 or Lync Server 2013 Edge Server, you need to add a new hosting provider, Microsoft Lync Online, and then set up hosting provider federation between your organization and Lync Online.</span></span>

  - <span data-ttu-id="13c24-114">Si votre environnement possède un serveur Edge Office Communications Server 2007 R2, vous devez configurer la Fédération SIP directe avec push.lync.com.</span><span class="sxs-lookup"><span data-stu-id="13c24-114">If your environment has a Office Communications Server 2007 R2 Edge Server, you need to set up direct SIP federation with push.lync.com.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13c24-115">Push.lync.com est un domaine Microsoft Office 365 pour le service de notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-115">Push.lync.com is a Microsoft Office 365 domain for Push Notification Service.</span></span>

    
    </div>

  - <span data-ttu-id="13c24-116">Pour activer les notifications de transmission, vous devez exécuter l’applet **de cmdlet Set-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="13c24-116">To enable push notifications, you need to run the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="13c24-117">Par défaut, les notifications push sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="13c24-117">By default, push notifications are turned off.</span></span>

  - <span data-ttu-id="13c24-118">Testez la configuration de la Fédération et les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-118">Test the federation configuration and push notifications.</span></span>

<div>

## <a name="to-configure-for-push-notifications-with-lync-server-2013-or-lync-server-2010-edge-server"></a><span data-ttu-id="13c24-119">Pour configurer les notifications de transmission avec Lync Server 2013 ou Lync Server 2010 Edge Server</span><span class="sxs-lookup"><span data-stu-id="13c24-119">To configure for push notifications with Lync Server 2013 or Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="13c24-120">Connectez-vous à un ordinateur sur lequel Lync Server Management Shell et OCSCore sont installés en tant que membre du groupe RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="13c24-120">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="13c24-121">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="13c24-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="13c24-122">Ajoutez un fournisseur d’hébergement Lync Server online.</span><span class="sxs-lookup"><span data-stu-id="13c24-122">Add a Lync Server online hosting provider.</span></span> <span data-ttu-id="13c24-123">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-123">At the command line, type:</span></span>
    
        New-CsHostingProvider -Identity <unique identifier for Lync Online hosting provider> -Enabled $True -ProxyFqdn <FQDN for the Access Server used by the hosting provider> -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="13c24-124">Exemple :</span><span class="sxs-lookup"><span data-stu-id="13c24-124">For example:</span></span>
    
        New-CsHostingProvider -Identity "LyncOnline" -Enabled $True -ProxyFqdn "sipfed.online.lync.com" -VerificationLevel UseSourceVerification
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="13c24-125">Vous ne pouvez pas avoir plusieurs relations de Fédération avec un seul fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="13c24-125">You cannot have more than one federation relationship with a single hosting provider.</span></span> <span data-ttu-id="13c24-126">Autrement dit, si vous avez déjà configuré un fournisseur d’hébergement ayant une relation de Fédération avec sipfed.online.lync.com, n’ajoutez pas d’autre fournisseur d’hébergement, même si l’identité du fournisseur d’hébergement n’est pas LyncOnline.</span><span class="sxs-lookup"><span data-stu-id="13c24-126">That is, if you have already set up a hosting provider that has a federation relationship with sipfed.online.lync.com, do not add another hosting provider for it, even if the identity of the hosting provider is something other than LyncOnline.</span></span>

    
    </div>

4.  <span data-ttu-id="13c24-127">Configurez la Fédération des fournisseurs d’hébergement entre votre organisation et le service de notifications de transmission de Lync Online.</span><span class="sxs-lookup"><span data-stu-id="13c24-127">Set up hosting provider federation between your organization and the Push Notification Service at Lync Online.</span></span> <span data-ttu-id="13c24-128">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-128">At the command line, type:</span></span>
    
        New-CsAllowedDomain -Identity "push.lync.com"

</div>

<div>

## <a name="to-configure-for-push-notifications-with-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="13c24-129">Pour configurer les notifications de transmission avec un serveur Edge Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="13c24-129">To configure for push notifications with Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="13c24-130">Ouvrez une session sur le serveur Edge en tant que membre du groupe RtcUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="13c24-130">Log on to the Edge Server as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="13c24-131">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Outils d’administration**, puis sur gestion de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="13c24-131">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Computer Management**.</span></span>

3.  <span data-ttu-id="13c24-132">Dans l’arborescence de la console, développez **services et applications**, cliquez avec le bouton droit sur **Microsoft Office Communications Server 2007 R2**, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="13c24-132">In the console tree, expand **Services and Applications**, right-click **Microsoft Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="13c24-133">Dans l’onglet **autoriser** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="13c24-133">On the **Allow** tab, click **Add**.</span></span>

5.  <span data-ttu-id="13c24-134">Dans la boîte de dialogue **Ajouter un partenaire fédéré** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="13c24-134">In the **Add Federated Partner** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="13c24-135">Dans **nom de domaine du partenaire fédéré**, entrez **push.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="13c24-135">In **Federated partner domain name**, type **push.lync.com**.</span></span>
    
      - <span data-ttu-id="13c24-136">Dans **serveur Edge d’accès du partenaire fédéré**, entrez **sipfed.online.Lync.com**.</span><span class="sxs-lookup"><span data-stu-id="13c24-136">In **Federated partner Access Edge Server**, type **sipfed.online.lync.com**.</span></span>
    
      - <span data-ttu-id="13c24-137">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="13c24-137">Click **OK**.</span></span>

</div>

<div>

## <a name="to-enable-push-notifications"></a><span data-ttu-id="13c24-138">Pour activer les notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="13c24-138">To enable push notifications</span></span>

1.  <span data-ttu-id="13c24-139">Connectez-vous à un ordinateur sur lequel Lync Server Management Shell et OCSCore sont installés en tant que membre du rôle CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="13c24-139">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="13c24-140">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="13c24-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="13c24-141">Activez les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-141">Enable push notifications.</span></span> <span data-ttu-id="13c24-142">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-142">At the command line, type:</span></span>
    
        Set-CsPushNotificationConfiguration -EnableApplePushNotificationService $True -EnableMicrosoftPushNotificationService $True

4.  <span data-ttu-id="13c24-143">Activez la Fédération.</span><span class="sxs-lookup"><span data-stu-id="13c24-143">Enable federation.</span></span> <span data-ttu-id="13c24-144">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-144">At the command line, type:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-test-federation-and-push-notifications"></a><span data-ttu-id="13c24-145">Pour tester la Fédération et les notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="13c24-145">To test federation and push notifications</span></span>

1.  <span data-ttu-id="13c24-146">Connectez-vous à un ordinateur sur lequel Lync Server Management Shell et OCSCore sont installés en tant que membre du rôle CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="13c24-146">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="13c24-147">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="13c24-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="13c24-148">Testez la configuration de la Fédération.</span><span class="sxs-lookup"><span data-stu-id="13c24-148">Test the federation configuration.</span></span> <span data-ttu-id="13c24-149">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-149">At the command line, type:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn <FQDN of Access Edge server used for federated SIP traffic> -Domain <FQDN of federated domain> -ProxyFqdn <FQDN of the Access Edge server used by the federated organization>
    
    <span data-ttu-id="13c24-150">Exemple :</span><span class="sxs-lookup"><span data-stu-id="13c24-150">For example:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn accessproxy.contoso.com -Domain push.lync.com -ProxyFqdn sipfed.online.lync.com

4.  <span data-ttu-id="13c24-151">Testez les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="13c24-151">Test push notifications.</span></span> <span data-ttu-id="13c24-152">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="13c24-152">At the command line, type:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn <Access Edge service FQDN>
    
    <span data-ttu-id="13c24-153">Exemple :</span><span class="sxs-lookup"><span data-stu-id="13c24-153">For example:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn accessproxy.contoso.com

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="13c24-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13c24-154">See Also</span></span>


[<span data-ttu-id="13c24-155">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="13c24-155">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
[<span data-ttu-id="13c24-156">Test-CsMcxPushNotification</span><span class="sxs-lookup"><span data-stu-id="13c24-156">Test-CsMcxPushNotification</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification)  
  

<span data-ttu-id="13c24-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13c24-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

