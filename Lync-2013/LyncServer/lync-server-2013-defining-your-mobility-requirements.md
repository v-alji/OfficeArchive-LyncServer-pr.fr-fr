---
title: 'Lync Server 2013 : Définition de la configuration requise pour la mobilité'
description: 'Lync Server 2013 : définir vos exigences de mobilité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your mobility requirements
ms:assetid: b7608335-cdeb-4aae-8e4b-d80c55f0d62b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690039(v=OCS.15)
ms:contentKeyID: 48185226
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fbc1a443946f0c879397f41628cfe788b428ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430895"
---
# <a name="defining-your-mobility-requirements-for-lync-server-2013"></a><span data-ttu-id="f32fa-103">Définition de la configuration requise pour la mobilité pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-103">Defining your mobility requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f32fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f32fa-104">

<span> </span></span></span>

<span data-ttu-id="f32fa-105">_**Dernière modification de la rubrique :** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="f32fa-105">_**Topic Last Modified:** 2013-02-14_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="f32fa-106">Pendant la phase de planification de la fonctionnalité de mobilité de Lync Server 2013, lorsque vous utilisez les clients mobiles Lync 2010 mobile et Lync 2013, vous prenez des décisions qui déterminent vos étapes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f32fa-106">During the planning phase for the Lync Server 2013 mobility feature, when you are using Lync 2010 Mobile and Lync 2013 Mobile clients, you make decisions that determine your deployment steps.</span></span>

<span data-ttu-id="f32fa-107">Voici les décisions que vous devez prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="f32fa-107">Here are the decisions that you must consider:</span></span>

  - <span data-ttu-id="f32fa-108">**Voulez-vous utiliser la découverte automatique pour les clients mobiles Lync ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-108">**Do you want to use automatic discovery for Lync mobile clients?**</span></span>
    
    <span data-ttu-id="f32fa-109">Si vous voulez prendre en charge la découverte automatique, vous devez créer des enregistrements DNS internes et externes, ajouter d’autres noms d’objet aux certificats sur les serveurs frontaux, les directeurs et le proxy inverse, puis modifier les règles de publication existantes sur le proxy inverse.</span><span class="sxs-lookup"><span data-stu-id="f32fa-109">If you want to support automatic discovery, you need to create new internal and external Domain Name System (DNS) records, add subject alternative names to certificates on the Front End Servers, Directors, and reverse proxy, and modify the existing publishing rules on the reverse proxy.</span></span> <span data-ttu-id="f32fa-110">Pour plus d’informations, voir [Configuration requise pour la mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="f32fa-110">For details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="f32fa-111">La découverte automatique permet aux utilisateurs de retrouver automatiquement les services Web Lync Server 2013 à partir de n’importe où, à l’intérieur ou à l’extérieur du réseau d’entreprise, sans entrer d’URL dans leurs paramètres d’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f32fa-111">With automatic discovery, users can automatically locate Lync Server 2013 Web Services from anywhere inside or outside the corporate network, without entering URLs in their mobile device settings.</span></span>
    
    <span data-ttu-id="f32fa-112">Si vous utilisez les paramètres manuels au lieu de la découverte automatique, les utilisateurs mobiles doivent entrer manuellement les URL suivantes dans leurs appareils mobiles :</span><span class="sxs-lookup"><span data-stu-id="f32fa-112">If you use manual settings instead of automatic discovery, mobile users need to manually enter the following URLs in their mobile devices:</span></span>
    
      - <span data-ttu-id="f32fa-113"> https:// \<ExtPoolFQDN\> /Autodiscover/autodiscoverservice.svc/root pour l’accès externe</span><span class="sxs-lookup"><span data-stu-id="f32fa-113">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>
    
      - <span data-ttu-id="f32fa-114"> https:// \<IntPoolFQDN\> /Autodiscover/autodiscoverservice. svc/root pour l’accès interne</span><span class="sxs-lookup"><span data-stu-id="f32fa-114">https://\<IntPoolFQDN\>/AutoDiscover/ autodiscoverservice.svc/Root for internal access</span></span>
    
    <span data-ttu-id="f32fa-115">Nous vous recommandons vivement d’utiliser la découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="f32fa-115">We strongly recommend using automatic discovery.</span></span> <span data-ttu-id="f32fa-116">Pour résoudre les problèmes, le principal recours aux paramètres manuels.</span><span class="sxs-lookup"><span data-stu-id="f32fa-116">The primary use of manual settings is for troubleshooting.</span></span>

  - <span data-ttu-id="f32fa-117">**Si vous décidez de prendre en charge la découverte automatique, êtes-vous prêt à mettre à jour les certificats du proxy inverse avec des noms de remplacement pour chaque domaine SIP ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-117">**If you decide to support automatic discovery, are you willing to update certificates on the reverse proxy with subject alternative names for each SIP domain?**</span></span>
    
    <span data-ttu-id="f32fa-118">Si vous avez de nombreux domaines SIP, la mise à jour des certificats publics sur le proxy inverse peut devenir très onéreuse.</span><span class="sxs-lookup"><span data-stu-id="f32fa-118">If you have many SIP domains, updating public certificates on the reverse proxy can become very expensive.</span></span> <span data-ttu-id="f32fa-119">Si tel est le cas, vous pouvez choisir d’implémenter la découverte automatique de manière à ce que la demande de service de découverte automatique initiale utilise HTTP sur le port 80, au lieu d’utiliser HTTPs sur le port 443.</span><span class="sxs-lookup"><span data-stu-id="f32fa-119">If this is the case, you can choose to implement automatic discovery so that the initial Autodiscover Service request uses HTTP on port 80, instead of using HTTPS on port 443.</span></span> <span data-ttu-id="f32fa-120">Toutefois, il ne s’agit pas de l’approche recommandée.</span><span class="sxs-lookup"><span data-stu-id="f32fa-120">However, this is not the recommended approach.</span></span> <span data-ttu-id="f32fa-121">Si vous décidez d’en choisir une autre, vous n’avez pas besoin de mettre à jour les certificats sur le proxy inverse, mais vous devez créer une règle de publication Web pour HTTP sur le port 80.</span><span class="sxs-lookup"><span data-stu-id="f32fa-121">If you decide to choose this alternative, you do not need to update the certificates on the reverse proxy, but you need to create a web publishing rule for HTTP on port 80.</span></span> <span data-ttu-id="f32fa-122">Pour en savoir plus, voir [exigences techniques en matière de mobilité dans Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="f32fa-122">For more details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="f32fa-123">**Souhaitez-vous prendre en charge les clients mobiles Lync à la fois internes et externes au réseau d’entreprise, ou les clients de support technique uniquement à l’intérieur du réseau d’entreprise ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-123">**Do you want to support Lync mobile clients both internal and external to the corporate network, or support clients only inside the corporate network?**</span></span>
    
    <span data-ttu-id="f32fa-124">Si vous voulez prendre en charge les clients mobiles internes et externes à votre réseau, les appareils mobiles peuvent accéder aux fonctionnalités de mobilité depuis n’importe quel emplacement.</span><span class="sxs-lookup"><span data-stu-id="f32fa-124">If you want to support mobile clients internal and external to your network, mobile devices can access mobility features from any location.</span></span> <span data-ttu-id="f32fa-125">La configuration par défaut consiste à prendre en charge les clients internes et externes au réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f32fa-125">The default configuration is to support clients both internal and external to the corporate network.</span></span>
    
    <span data-ttu-id="f32fa-126">Même si la configuration par défaut permet au trafic du client mobile de traverser le site externe, vous pouvez limiter le trafic client mobile au réseau d’entreprise interne.</span><span class="sxs-lookup"><span data-stu-id="f32fa-126">Although the default configuration enables mobile client traffic to go through the external site, you can restrict mobile client traffic to the internal corporate network.</span></span> <span data-ttu-id="f32fa-127">Lorsque vous restreignez le trafic vers le réseau interne, les utilisateurs peuvent utiliser les applications mobiles Lync sur leur appareil mobile uniquement lorsqu’elles se trouvent à l’intérieur du réseau.</span><span class="sxs-lookup"><span data-stu-id="f32fa-127">When you restrict the traffic to the internal network, users can use Lync mobile applications on their mobile devices only when they are inside the network.</span></span>
    
    <span data-ttu-id="f32fa-128">Pour les déploiements prenant en charge la mobilité à l’aide du service de mobilité MCX et de Lync 2010 mobile, vous exécutez l’applet **de passe Set-CsMcxConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f32fa-128">For deployments that support mobility using the Mcx mobility service and Lync 2010 Mobile, you run the **Set-CsMcxConfiguration** cmdlet.</span></span> <span data-ttu-id="f32fa-129">Pour définir la mobilité pour une utilisation interne uniquement, vous devez utiliser une commande semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="f32fa-129">To set mobility for internal use only, you would use a command similar to the following:</span></span>
    
        Set-CsMcxConfiguration -Identity site:Redmond -ExposedWebURL Internal
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f32fa-130">Aucune configuration supplémentaire n’est requise pour UCWA.</span><span class="sxs-lookup"><span data-stu-id="f32fa-130">There are no additional configurations required for UCWA.</span></span> <span data-ttu-id="f32fa-131">UCWA n’a pas de configuration équivalente en interne.</span><span class="sxs-lookup"><span data-stu-id="f32fa-131">UCWA does not have an equivalent internal-only configuration.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f32fa-132">Si vous utilisez un &nbsp; serveur frontal ou une grappes frontale Lync server 2013, <STRONG>et que vous n’avez pas</STRONG> de &nbsp; serveurs frontaux 2010 Lync Server ou de pools frontal, il n' <STRONG>est pas nécessaire de disposer de la persistance basée sur le cookie</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f32fa-132">If you are using a Lync Server 2013&nbsp;Front End Server or Front End pools and <STRONG>you do not have</STRONG> any Lync Server 2010&nbsp;Front End Servers or Front End pools, <STRONG>there is no requirement for cookie-based persistence</STRONG>.</span></span> <span data-ttu-id="f32fa-133">Si vous avez besoin de conserver un serveur frontal ou un pool frontal de Lync Server 2010 &nbsp; , les mêmes règles s’appliquent également à celle de Lync server 2010 pour la persistance basée sur les cookies.</span><span class="sxs-lookup"><span data-stu-id="f32fa-133">If you need to retain any Lync Server 2010&nbsp;Front End Servers or Front End pools, the same rules still apply as in Lync Server 2010 for cookie-based persistence.</span></span>

    
    </div>

  - <span data-ttu-id="f32fa-134">**Souhaitez-vous prendre en charge les notifications de transmission pour les appareils Apple iOS et Windows Phone ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-134">**Do you want to support push notifications for Apple iOS devices and Windows Phones?**</span></span>
    
    <span data-ttu-id="f32fa-135">Si vous prenez en charge les notifications de transmission, les appareils Apple iOS et les téléphones Windows pris en charge reçoivent une notification d’événements qui se produisent lorsque l’application mobile est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f32fa-135">If you support push notifications, supported Apple iOS devices and Windows Phones receive a notification of events that occur when the mobile application is inactive.</span></span> <span data-ttu-id="f32fa-136">Vous devez configurer votre serveur Edge pour qu’il dispose d’une relation de Fédération avec le service de notification Poussée de Lync Server sur le Cloud, qui se trouve dans Lync Online datacenter et qu’il exécute une cmdlet pour activer les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="f32fa-136">You must configure your Edge Server to have a federation relationship with the cloud-based Lync Server Push Notification Service, which is located in the Lync Online datacenter, and run a cmdlet to enable push notifications.</span></span>
    
    <span data-ttu-id="f32fa-137">Si vous voulez prendre en charge les notifications de transmission sur votre réseau Wi-Fi, en plus de la prise en charge des notifications de transmission sur les réseaux 3G ou de données des fournisseurs d’appareils mobiles, vous devez ouvrir le port 5223 sortant sur votre entreprise Wi-Fi réseau.</span><span class="sxs-lookup"><span data-stu-id="f32fa-137">If you want to support push notifications over your Wi-Fi network, in addition to supporting push notifications over the mobile device providers' 3G or data networks, you must open port 5223 outbound on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="f32fa-138">La prise en charge des notifications de transmission sur le réseau Wi-Fi prend en charge les appareils mobiles qui utilisent uniquement des Wi-Fi et des appareils mobiles présentant une mauvaise réception en intérieur.</span><span class="sxs-lookup"><span data-stu-id="f32fa-138">Supporting push notifications over the Wi-Fi network supports mobile devices that use only Wi-Fi and mobile devices that have poor indoor reception.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f32fa-139">L’ouverture du port TCP 5223 est requise uniquement lors de la prise en charge des appareils Apple exécutant le client mobile Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="f32fa-139">Opening port TCP 5223 is required only when supporting Apple devices running the Lync 2010 Mobile client.</span></span>

    
    </div>
    
    <span data-ttu-id="f32fa-140">Si vous ne prenez pas en charge les notifications de transmission, les utilisateurs des appareils mobiles Apple et des téléphones Windows ne seront pas en mesure de détecter les événements, tels que les invitations aux messages instantanés ou les messages manqués, qui se produisent lorsque l’application mobile est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f32fa-140">If you do not support push notifications, users of Apple mobile devices and Windows Phones will not find out about events—such as instant message invitations or missed messages—that occur when the mobile application is inactive.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f32fa-141">Les clients mobiles Lync 2013 sur les appareils Apple ne requièrent aucune notification de transmission.</span><span class="sxs-lookup"><span data-stu-id="f32fa-141">Lync 2013 Mobile clients on Apple devices do not require push notification.</span></span> <span data-ttu-id="f32fa-142">Les clients mobiles Lync 2013 sur Windows Phone utilisent une notification de transmission.</span><span class="sxs-lookup"><span data-stu-id="f32fa-142">The Lync 2013 Mobile clients on Windows Phone use push notification.</span></span> <span data-ttu-id="f32fa-143">La planification de la notification de transmission et du centre de notifications de transmission de notifications reste inchangée pour les appareils mobiles Lync sur Windows Phone et Apple qui ne peuvent pas exécuter le client mobile Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="f32fa-143">Planning for push notification and the push notification clearinghouse remain the same for Lync Mobile on Windows Phone and Apple devices that are not able to run the Lync 2013 Mobile client.</span></span>

    
    </div>

  - <span data-ttu-id="f32fa-144">**Souhaitez-vous que tous les utilisateurs aient accès aux fonctionnalités de mobilité ou vous voulez peut-être spécifier les utilisateurs qui ont accès à ces fonctionnalités ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-144">**Do you want all users to have access to mobility features, or do you want to be able to specify which users have access to these features?**</span></span>
    
    <span data-ttu-id="f32fa-145">Ce tableau décrit les fonctionnalités accessibles aux utilisateurs de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f32fa-145">The table describes features available to users in Lync Server 2013.</span></span> <span data-ttu-id="f32fa-146">Les valeurs par défaut autorisent les appels via le bureau, autorisez la voix sur IP (VoIP) et activez la mobilité.</span><span class="sxs-lookup"><span data-stu-id="f32fa-146">The defaults allow Call via Work, allow Voice over IP (VoIP), and enable Mobility.</span></span> <span data-ttu-id="f32fa-147">Voici l’ensemble complet des options disponibles :</span><span class="sxs-lookup"><span data-stu-id="f32fa-147">Here is the full set of available options:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f32fa-148">Fonction/nom/paramètre de la fonction (les noms des paramètres de stratégie ne sont pas identiques)</span><span class="sxs-lookup"><span data-stu-id="f32fa-148">Feature/Parameter Name/Scope (Policy parameter names may not be the same)</span></span></th>
    <th><span data-ttu-id="f32fa-149">Description</span><span class="sxs-lookup"><span data-stu-id="f32fa-149">Description</span></span></th>
    <th><span data-ttu-id="f32fa-150">Introduis</span><span class="sxs-lookup"><span data-stu-id="f32fa-150">Introduced</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f32fa-151">Activer la mobilité</span><span class="sxs-lookup"><span data-stu-id="f32fa-151">Enable Mobility</span></span></p>
    <p><span data-ttu-id="f32fa-152">Nom du paramètre : <code>EnableMobility</code></span><span class="sxs-lookup"><span data-stu-id="f32fa-152">Parameter Name : <code>EnableMobility</code></span></span></p>
    <p><span data-ttu-id="f32fa-153">Étendue : Global/site/utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32fa-153">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-154">Paramètre d’administration pour contrôler les utilisateurs au sein d’une étendue donnée sur laquelle Lync mobile n’est pas installé, si la stratégie est définie sur false, l’utilisateur ne peut pas se connecter au client.</span><span class="sxs-lookup"><span data-stu-id="f32fa-154">Administrative setting to control users in a given scope that have the Lync Mobile installed, If the policy is set to False, the user would not be able to sign into the client.</span></span></p>
    <p><span data-ttu-id="f32fa-155">Le paramètre par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="f32fa-155">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-156">Mise à jour cumulative pour Lync Server 2010:2011 novembre</span><span class="sxs-lookup"><span data-stu-id="f32fa-156">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f32fa-157">Activer les appels vocaux extérieurs</span><span class="sxs-lookup"><span data-stu-id="f32fa-157">Enable Outside Voice</span></span></p>
    <p><span data-ttu-id="f32fa-158">Nom du paramètre : <code>EnableOutsideVoice</code></span><span class="sxs-lookup"><span data-stu-id="f32fa-158">Parameter Name : <code>EnableOutsideVoice</code></span></span></p>
    <p><span data-ttu-id="f32fa-159">Étendue : Global/site/utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32fa-159">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-160">Contrôle la capacité d’un utilisateur à utiliser appel via le bureau, une fonctionnalité qui permet aux utilisateurs de passer et de recevoir des appels en utilisant leur numéro de téléphone plutôt que leur numéro de téléphone mobile.</span><span class="sxs-lookup"><span data-stu-id="f32fa-160">Controls a user’s ability to use Call Via Work, a feature that enables users to make and receive calls by using their work number instead of their mobile number.</span></span> <span data-ttu-id="f32fa-161">Si elle est définie sur false, l’utilisateur ne pourra pas passer ou recevoir des appels en utilisant son numéro de téléphone sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f32fa-161">If set to False, the user will not be able to make or receive calls by using their work number from their mobile device.</span></span></p>
    <p><span data-ttu-id="f32fa-162">Le paramètre par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="f32fa-162">The default setting is True</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-163">Mise à jour cumulative pour Lync Server 2010:2011 novembre</span><span class="sxs-lookup"><span data-stu-id="f32fa-163">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f32fa-164">Activer l’audio/la vidéo IP</span><span class="sxs-lookup"><span data-stu-id="f32fa-164">Enable IP Audio and Video</span></span></p>
    <p><span data-ttu-id="f32fa-165">Nom du paramètre : <code>EnableIPAudioVideo</code></span><span class="sxs-lookup"><span data-stu-id="f32fa-165">Parameter Name : <code>EnableIPAudioVideo</code></span></span></p>
    <p><span data-ttu-id="f32fa-166">Étendue : Global/site/utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32fa-166">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-167">Contrôle si un utilisateur peut utiliser le protocole VoIP pour passer ou recevoir des appels vocaux ou vidéo sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f32fa-167">Controls whether a user can use VoIP to make or receive voice or video calls on their mobile device.</span></span> <span data-ttu-id="f32fa-168">Si elle est définie sur false, l’utilisateur n’est pas en mesure de passer ou de recevoir des appels VoIP ou vidéo sur son appareil.</span><span class="sxs-lookup"><span data-stu-id="f32fa-168">If set to False, the user will not be able to make or receive VoIP or video calls on their device.</span></span></p>
    <p><span data-ttu-id="f32fa-169">Le paramètre par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="f32fa-169">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-170">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-170">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f32fa-171">Exiger WiFi pour l’audio IP</span><span class="sxs-lookup"><span data-stu-id="f32fa-171">Require WiFi for IP Audio</span></span></p>
    <p><span data-ttu-id="f32fa-172">Nom du paramètre : <code>RequireWiFiForIPAudio</code></span><span class="sxs-lookup"><span data-stu-id="f32fa-172">Parameter Name : <code>RequireWiFiForIPAudio</code></span></span></p>
    <p><span data-ttu-id="f32fa-173">Étendue : Global/site/utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32fa-173">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-174">Ce paramètre détermine si le client est tenu d’émettre et de recevoir des appels sur le protocole VoIP sur réseau WiFi plutôt que sur le réseau de données cellulaires.</span><span class="sxs-lookup"><span data-stu-id="f32fa-174">This setting defines whether the client will be required to make and receive calls over VoIP on WiFi instead of the cellular data network.</span></span> <span data-ttu-id="f32fa-175">S’il est défini sur true, l’utilisateur peut passer et recevoir des appels VoIP uniquement lorsqu’il est connecté à un réseau WiFi.</span><span class="sxs-lookup"><span data-stu-id="f32fa-175">If set to True, the user can make and receive VoIP calls only when connected to a WiFi network.</span></span></p>
    <p><span data-ttu-id="f32fa-176">Le paramètre par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="f32fa-176">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-177">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-177">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f32fa-178">Exiger WiFi pour la vidéo IP</span><span class="sxs-lookup"><span data-stu-id="f32fa-178">Require WiFi for IP Video</span></span></p>
    <p><span data-ttu-id="f32fa-179">Nom du paramètre : <code>RequireWiFiForIPVideo</code></span><span class="sxs-lookup"><span data-stu-id="f32fa-179">Parameter Name : <code>RequireWiFiForIPVideo</code></span></span></p>
    <p><span data-ttu-id="f32fa-180">Étendue : Global/site/utilisateur</span><span class="sxs-lookup"><span data-stu-id="f32fa-180">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-181">Ce paramètre détermine si le client est tenu d’émettre et de recevoir des appels vidéo sur Wi-Fi plutôt que sur le réseau de données cellulaires.</span><span class="sxs-lookup"><span data-stu-id="f32fa-181">This setting defines whether the client will be required to make and receive video calls on Wi-Fi instead of on the cellular data network.</span></span> <span data-ttu-id="f32fa-182">S’il est défini sur true, l’utilisateur peut passer et recevoir des appels vidéo uniquement lorsqu’il est connecté à un réseau Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f32fa-182">If set to True, the user can make and receive video calls only when connected to a Wi-Fi network.</span></span></p>
    <p><span data-ttu-id="f32fa-183">Le paramètre par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="f32fa-183">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="f32fa-184">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-184">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="f32fa-185">Pour obtenir une description des paramètres de stratégie que vous pouvez configurer et sur la gestion des stratégies, voir [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) et [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span><span class="sxs-lookup"><span data-stu-id="f32fa-185">For a description of the policy settings that you can configure, and how to manage the policies, see [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) and [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span></span>

  - <span data-ttu-id="f32fa-186">**Souhaitez-vous que les utilisateurs qui n’ont pas été activés pour voix entreprise puissent utiliser le Cliquer pour rejoindre des conférences ?**</span><span class="sxs-lookup"><span data-stu-id="f32fa-186">**Do you want users who are not enabled for Enterprise Voice to be able to use Click to Join to join conferences?**</span></span>
    
    <span data-ttu-id="f32fa-187">Pour que les utilisateurs puissent accéder aux fonctionnalités de mobilité et aux appels via le bureau, ils doivent être activés pour voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="f32fa-187">For users to have access to mobility features and Call via Work, they must be enabled for Enterprise Voice.</span></span> <span data-ttu-id="f32fa-188">Toutefois, les utilisateurs qui ne sont pas autorisés à utiliser la voix entreprise peuvent participer à des conférences en cliquant sur le lien sur leur appareil mobile, s’ils disposent d’une stratégie vocale appropriée.</span><span class="sxs-lookup"><span data-stu-id="f32fa-188">However, users who are not enabled for Enterprise Voice can join conferences by clicking the link on their mobile device, if they have an appropriate voice policy assigned to them.</span></span> <span data-ttu-id="f32fa-189">Vous pouvez affecter une stratégie vocale spécifique à ces utilisateurs ou vérifier qu’une stratégie globale ou une stratégie de niveau de site existe qui s’appliquent à ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f32fa-189">You can either assign a specific voice policy to these users or make sure that a global policy or site-level policy exists that applies to them.</span></span> <span data-ttu-id="f32fa-190">La stratégie vocale que vous attribuez doit avoir des enregistrements et des itinéraires d’utilisation de réseau téléphonique commuté (RTC) pour permettre aux utilisateurs de participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="f32fa-190">The voice policy that you assign must have public switched telephone network (PSTN) usage records and routes that define the areas to which users can dial out to join a conference.</span></span> <span data-ttu-id="f32fa-191">Pour plus d’informations sur la configuration de la stratégie vocale, des enregistrements d’utilisation RTC et des itinéraires, voir [Configuration des stratégies vocales, des enregistrements d’utilisation RTC et des itinéraires vocaux dans Lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span><span class="sxs-lookup"><span data-stu-id="f32fa-191">For details about setting voice policy, PSTN usage records, and routes, see [Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f32fa-192">Les utilisateurs mobiles qui souhaitent utiliser l’option Cliquer pour rejoindre requièrent une stratégie vocale, ainsi que les enregistrements d’utilisation RTC et les itinéraires vocaux correspondants, car le fait de cliquer sur le lien sur l’appareil mobile génère un appel sortant de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f32fa-192">Mobile users who want to use Click to Join require a voice policy, along with the related PSTN usage records and voice routes, because clicking the link on the mobile device results in an outbound call from Lync Server 2013.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="f32fa-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f32fa-193">See Also</span></span>


[<span data-ttu-id="f32fa-194">Exigences techniques pour la mobilité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-194">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  


[<span data-ttu-id="f32fa-195">Configuration des stratégies vocales, des enregistrements d’utilisation RTC et des itinéraires vocaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f32fa-195">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="f32fa-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f32fa-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

