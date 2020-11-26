---
title: 'Lync Server 2013 : configuration de la bande passante vidéo'
description: 'Lync Server 2013 : configuration de la bande passante vidéo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring video bandwidth in Lync Server
ms:assetid: 446bed91-b26f-4ab2-b2f5-36e6810b405b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204842(v=OCS.15)
ms:contentKeyID: 48183984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85fedbe2fb856696236e79c3bbcece34d5af4a34
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432414"
---
# <a name="configuring-video-bandwidth-in-lync-server-2013"></a><span data-ttu-id="03fb1-103">Configuration de la bande passante vidéo dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03fb1-103">Configuring video bandwidth in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03fb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03fb1-104">

<span> </span></span></span>

<span data-ttu-id="03fb1-105">_**Dernière modification de la rubrique :** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="03fb1-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="03fb1-106">Lync Server 2013 inclut plusieurs paramètres pour la gestion de la vidéo pour les appels et les conférences à plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="03fb1-106">Lync Server 2013 includes several settings for managing video for two-party calls and multiparty conferences.</span></span> <span data-ttu-id="03fb1-107">Lorsque vous déployez Lync Server 2013, vous devez déterminer si les paramètres par défaut sont appropriés pour votre organisation, et les modifier si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="03fb1-107">When you deploy Lync Server 2013, you should evaluate whether the default settings are appropriate for your organization, and modify them as necessary.</span></span>

<span data-ttu-id="03fb1-108">Les paramètres décrits dans cette section s’appliquent aux appels à deux participants et aux conférences multiparties.</span><span class="sxs-lookup"><span data-stu-id="03fb1-108">The parameters described in this section apply to both two-party calls and multiparty conferencing.</span></span> <span data-ttu-id="03fb1-109">Pour afficher ou modifier ces paramètres, utilisez l’une des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="03fb1-109">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="03fb1-110">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="03fb1-110">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="03fb1-111">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="03fb1-111">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="03fb1-112">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="03fb1-112">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="03fb1-113">Vérifiez les paramètres suivants dans votre stratégie de conférence :</span><span class="sxs-lookup"><span data-stu-id="03fb1-113">Verify the following settings in your conferencing policy:</span></span>

  - <span data-ttu-id="03fb1-114">**VideoBitRateKb**   Ce paramètre spécifie le débit vidéo maximal en kilobits par seconde (Ko) utilisés pour la vidéo envoyée par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03fb1-114">**VideoBitRateKb**   This setting specifies the maximum video bit rate in kilobits per second (kbps) used for video sent by a user.</span></span> <span data-ttu-id="03fb1-115">La valeur par défaut est 50000 kb/s.</span><span class="sxs-lookup"><span data-stu-id="03fb1-115">The default value is 50000 kbps.</span></span> <span data-ttu-id="03fb1-116">Les valeurs valides sont comprises entre 0 et 50000.</span><span class="sxs-lookup"><span data-stu-id="03fb1-116">Valid values are 0 to 50000.</span></span>
    
    <span data-ttu-id="03fb1-117">Ce paramètre s’applique uniquement à la vidéo principale et à la vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="03fb1-117">This setting applies separately to main video and panoramic video.</span></span>
    
    <span data-ttu-id="03fb1-118">Exemple : Si vous spécifiez 2000 kbps, Lync Server peut envoyer 2000 kbps pour le flux vidéo principal et 2000 kbps pour le flux vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="03fb1-118">Example: if you specify 2000 kbps, then Lync Server can send 2000 kbps for the main video stream and 2000 kbps for the panoramic video stream.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="03fb1-119">La bande passante réseau vidéo maximale pour un point de terminaison Lync 2013 est 8000 kbps pour la vidéo principale et 2500 kbps pour la vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="03fb1-119">The maximum video network bandwidth for a Lync 2013 endpoint is 8000 kbps for the main video and 2500 kbps for panoramic video.</span></span> <span data-ttu-id="03fb1-120">Ces valeurs maximales sont atteintes uniquement si plusieurs vidéos sont reçues ou envoyées.</span><span class="sxs-lookup"><span data-stu-id="03fb1-120">These maximum values are reached only if multiple videos are received or sent.</span></span> <span data-ttu-id="03fb1-121">Pour plus d’informations, consultez la section « utilisation du réseau du trafic multimédia » dans <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">exigences de bande passante réseau pour le trafic multimédia dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="03fb1-121">For details, see the "Media Traffic Network Usage" section in <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">Network bandwidth requirements for media traffic in Lync Server 2013</A>.</span></span> <span data-ttu-id="03fb1-122">Cette section répertorie la bande passante du flux vidéo maximal et standard pour toutes les résolutions prises en charge.</span><span class="sxs-lookup"><span data-stu-id="03fb1-122">This section lists the maximum and typical video stream bandwidth for all supported resolutions.</span></span>

    
    </div>

  - <span data-ttu-id="03fb1-123">**TotalReceiveVideoBitRateKb**   Ce paramètre, qui est une nouveauté de Lync Server 2013, spécifie le débit maximal autorisé (en kilobits par seconde) pour tous les flux vidéo reçus par un client.</span><span class="sxs-lookup"><span data-stu-id="03fb1-123">**TotalReceiveVideoBitRateKb**   This setting, which is new in Lync Server 2013, specifies the maximum allowed bitrate (in kilobits per second) for all the video streams received by a client.</span></span> <span data-ttu-id="03fb1-124">C’est-à-dire qu’il spécifie le total combiné de tous les flux vidéo, à l’exception des flux vidéo panoramiques qu’un client peut recevoir.</span><span class="sxs-lookup"><span data-stu-id="03fb1-124">That is, it specifies the combined total for all the video streams, except for panoramic video streams, that a client can receive.</span></span> <span data-ttu-id="03fb1-125">Par exemple, si vous spécifiez 1500 kbps, un client peut recevoir jusqu’à 1500 kbps de vidéo, ce qui peut être composé de plusieurs flux vidéo ou d’un seul flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="03fb1-125">For example, if you specify 1500 kbps, then a client can receive up to 1500 kbps of video, which may consist of multiple video streams or a single video stream.</span></span> <span data-ttu-id="03fb1-126">Ce paramètre s’applique uniquement aux clients Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="03fb1-126">This setting applies only to Lync Server 2013 clients.</span></span>
    
    <span data-ttu-id="03fb1-127">La valeur par défaut de **TotalReceiveVideoBitRateKb** est 50000 kbps.</span><span class="sxs-lookup"><span data-stu-id="03fb1-127">The default value for **TotalReceiveVideoBitRateKb** is 50000 kbps.</span></span> <span data-ttu-id="03fb1-128">Si le paramètre **EnableMultiviewJoin** pour la vue Galerie est défini sur true, **TotalReceiveVideoBitRateKb** ne doit pas être défini sous 420 KB/s.</span><span class="sxs-lookup"><span data-stu-id="03fb1-128">If the **EnableMultiviewJoin** setting for Gallery View is set to True, **TotalReceiveVideoBitRateKb** must not be set below 420 kbps.</span></span> <span data-ttu-id="03fb1-129">Si le paramètre **EnableMultiviewJoin** pour la vue Galerie est défini sur false, **TotalReceiveVideoBitRateKb** ne doit pas être défini sous 100 kb/s.</span><span class="sxs-lookup"><span data-stu-id="03fb1-129">If the **EnableMultiviewJoin** setting for Gallery View is set to False, **TotalReceiveVideoBitRateKb** must not be set below 100 kbps.</span></span> <span data-ttu-id="03fb1-130">Si **EnableMultiviewJoin** est défini sur true et que vous définissez la valeur inférieure à 420 KB/s, les valeurs par défaut sont la valeur Threshold.</span><span class="sxs-lookup"><span data-stu-id="03fb1-130">If **EnableMultiviewJoin** is set to True and you set the value below 420 kbps, the values will default to the threshold value.</span></span> <span data-ttu-id="03fb1-131">Ce seuil permet d’éviter toute configuration intempestive qui peut entraîner une mauvaise utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03fb1-131">This threshold helps prevent accidental misconfiguration that might result in poor user experience.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="03fb1-132">Pour plus d’informations sur le paramètre <STRONG>EnableMultiviewJoin</STRONG> , voir <A href="lync-server-2013-configuring-gallery-view.md">configuration de l’affichage Galerie dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="03fb1-132">For details about the <STRONG>EnableMultiviewJoin</STRONG> setting, see <A href="lync-server-2013-configuring-gallery-view.md">Configuring Gallery View in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="03fb1-133">**MaxVideoConferencingResolution**   Ce paramètre n’est plus utilisé pour les clients Lync Server 2013 dans les conférences Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="03fb1-133">**MaxVideoConferencingResolution**   This parameter is no longer used for Lync Server 2013 clients in Lync Server 2013 conferences.</span></span> <span data-ttu-id="03fb1-134">Les conférences Lync Server 2013 utilisent les contrôles de débit binaire décrits plus haut dans cette section.</span><span class="sxs-lookup"><span data-stu-id="03fb1-134">Lync Server 2013 conferences use the bit rate controls described earlier in this section.</span></span> <span data-ttu-id="03fb1-135">Ce paramètre est toujours utilisé pour les clients hérités qui rejoignent une conférence Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="03fb1-135">This setting is still used for legacy clients joining a Lync Server 2013 conference.</span></span> <span data-ttu-id="03fb1-136">Ce paramètre détermine la résolution maximale autorisée pour les clients hérités dans les conférences organisées par des utilisateurs hébergés sur Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="03fb1-136">This parameter determines the maximum resolution allowed for legacy clients in conferences organized by users who are homed on Lync Server 2013.</span></span> <span data-ttu-id="03fb1-137">En d’autres termes, les clients hérités sont traités de la même façon que dans les versions précédentes de Lync Server ou d’Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="03fb1-137">That is, legacy clients are treated the same as they were in previous versions of Lync Server or Office Communications Server.</span></span>

<span data-ttu-id="03fb1-138">En plus des paramètres de stratégie de conférence qui s’appliquent aux utilisateurs, évaluez les paramètres de configuration multimédia.</span><span class="sxs-lookup"><span data-stu-id="03fb1-138">In addition to conferencing policy settings that apply to users, evaluate media configuration settings.</span></span> <span data-ttu-id="03fb1-139">Pour afficher ou modifier ces paramètres, utilisez l’une des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="03fb1-139">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="03fb1-140">**Get-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03fb1-140">**Get-CsMediaConfiguration**</span></span>

  - <span data-ttu-id="03fb1-141">**Set-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03fb1-141">**Set- CsMediaConfiguration**</span></span>

  - <span data-ttu-id="03fb1-142">**Nouveau-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="03fb1-142">**New- CsMediaConfiguration**</span></span>

<span data-ttu-id="03fb1-143">Vérifiez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="03fb1-143">Verify the following setting:</span></span>

  - <span data-ttu-id="03fb1-144">**MaxVideoRateAllowed**   Ce paramètre par pool spécifie le taux maximal auquel les signaux vidéo sont transférés aux points de terminaison client.</span><span class="sxs-lookup"><span data-stu-id="03fb1-144">**MaxVideoRateAllowed**   This per-pool setting specifies the maximum rate at which video signals will be transferred at the client endpoints.</span></span> <span data-ttu-id="03fb1-145">Il s’applique uniquement aux versions antérieures de clients Lync Server.</span><span class="sxs-lookup"><span data-stu-id="03fb1-145">It applies only to previous versions of Lync Server clients.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="03fb1-146">Les clients Lync Server 2013 ignorent ce paramètre et utilisent plutôt le paramètre TotalReceiveVideoBitRateKb de la stratégie de conférence.</span><span class="sxs-lookup"><span data-stu-id="03fb1-146">Lync Server 2013 clients ignore this setting and use the TotalReceiveVideoBitRateKb setting in conferencing policy instead.</span></span>

    
    </div>
    
    <span data-ttu-id="03fb1-147">La valeur par défaut est HD720P.</span><span class="sxs-lookup"><span data-stu-id="03fb1-147">The default value is HD720P.</span></span> <span data-ttu-id="03fb1-148">Les valeurs valides sont HD720p15M, VGA600K et CIF250K.</span><span class="sxs-lookup"><span data-stu-id="03fb1-148">Valid values are HD720p15M, VGA600K, and CIF250K.</span></span>
    
    <span data-ttu-id="03fb1-149">Exemple : Si vous spécifiez 1500 kbps, tous les clients hérités du pool peuvent recevoir jusqu’à 1500 kbps de vidéo dans le cadre de conférences à deux ou plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="03fb1-149">Example: If you specify 1500 kbps, then all the legacy clients in the pool can receive up to 1500 kbps of video in two-party or multiparty conferences.</span></span>

<span data-ttu-id="03fb1-150">Les procédures suivantes sont des exemples d’utilisation de Lync Server Management Shell pour modifier les paramètres décrits dans cette section.</span><span class="sxs-lookup"><span data-stu-id="03fb1-150">The following procedures are examples of using Lync Server Management Shell to modify the settings described in this section.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-video-settings"></a><span data-ttu-id="03fb1-151">Pour modifier la stratégie de conférence pour les paramètres vidéo</span><span class="sxs-lookup"><span data-stu-id="03fb1-151">To modify conferencing policy for video settings</span></span>

1.  <span data-ttu-id="03fb1-152">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-152">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="03fb1-153">Dans la ligne de commande, exécutez l’applet de commande suivante pour modifier la stratégie de conférence :</span><span class="sxs-lookup"><span data-stu-id="03fb1-153">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -VideoBitRateKb 2000 -TotalReceiveVideoBitRateKb 2000 

</div>

<div>

## <a name="to-modify-media-configuration-for-legacy-clients"></a><span data-ttu-id="03fb1-154">Pour modifier la configuration multimédia pour les clients hérités</span><span class="sxs-lookup"><span data-stu-id="03fb1-154">To modify media configuration for legacy clients</span></span>

1.  <span data-ttu-id="03fb1-155">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-155">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="03fb1-156">Dans la ligne de commande, exécutez l’applet de commande suivante pour modifier la configuration multimédia :</span><span class="sxs-lookup"><span data-stu-id="03fb1-156">At the command line, run the following cmdlet to edit the media configuration:</span></span>
    
        Set-CsMediaConfiguration -Identity site:Redmond01 -MaxVideoRateAllowed CIF250K

<span data-ttu-id="03fb1-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03fb1-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

