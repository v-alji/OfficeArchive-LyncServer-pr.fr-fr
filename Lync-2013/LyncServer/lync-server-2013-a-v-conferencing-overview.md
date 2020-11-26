---
title: Vue d’ensemble de la fonctionnalité de conférence A/V de Lync Server 2013
description: Vue d’ensemble de la fonction de conférence A/V de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: A/V conferencing overview
ms:assetid: 9583de87-4618-4a99-a47a-45e8cc4cc221
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619186(v=OCS.15)
ms:contentKeyID: 49733747
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76ef4f76a4df0187a7c36394b2c95e99876df9be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439549"
---
# <a name="overview-of-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="612d6-103">Présentation de la fonctionnalité de conférence A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="612d6-103">Overview of A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="612d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="612d6-104">

<span> </span></span></span>

<span data-ttu-id="612d6-105">_**Dernière modification de la rubrique :** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="612d6-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="612d6-106">La fonction de conférence A/V permet des communications audio et vidéo en temps réel entre vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="612d6-106">A/V conferencing enables real-time audio and video communications between your users.</span></span> <span data-ttu-id="612d6-107">Lorsque vous déployez des conférences, vous pouvez choisir d’activer et d’utiliser des conférences Web et des conférences A/V, ou uniquement des conférences Web.</span><span class="sxs-lookup"><span data-stu-id="612d6-107">When you deploy conferencing, you can choose to enable and use both web conferencing and A/V conferencing, or just web conferencing.</span></span>

<span data-ttu-id="612d6-108">Pour planifier votre conférence A/V, vous devez connaître la bande passante réseau nécessaire au type de trafic multimédia de conférence que requiert votre organisation.</span><span class="sxs-lookup"><span data-stu-id="612d6-108">To plan for A/V conferencing, you need to understand the network bandwidth required by the type of conferencing media that your organization requires.</span></span> <span data-ttu-id="612d6-109">Cela peut inclure l’audio, la vidéo et la vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="612d6-109">This could include audio, video, and panoramic video.</span></span>

<span data-ttu-id="612d6-110">Avant d’activer les utilisateurs pour les conférences A/V, assurez-vous que votre réseau peut gérer le chargement obtenu.</span><span class="sxs-lookup"><span data-stu-id="612d6-110">Before you enable users for A/V conferencing, ensure that your network can handle the resulting load.</span></span> <span data-ttu-id="612d6-111">Si la bande passante réseau est insuffisante, les performances du système seront largement diminuées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="612d6-111">Without sufficient network bandwidth, the user experience may be severely degraded.</span></span> <span data-ttu-id="612d6-112">Vous pouvez utiliser le contrôle d’admission des appels pour gérer la bande passante réseau utilisée par les conférences A/V.</span><span class="sxs-lookup"><span data-stu-id="612d6-112">You can use call admission control (CAC) to manage the network bandwidth used by A/V Conferencing.</span></span> <span data-ttu-id="612d6-113">Cela est important pour les réseaux restreints, comme les liaisons à bande passante limitée entre les sites centraux et les sites de succursale.</span><span class="sxs-lookup"><span data-stu-id="612d6-113">This is important for restricted networks, such as limited bandwidth links between central and branch sites.</span></span> <span data-ttu-id="612d6-114">Pour plus d’informations, voir [vue d’ensemble du contrôle d’admission des appels dans Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span><span class="sxs-lookup"><span data-stu-id="612d6-114">For details, see [Overview of call admission control in Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span></span> <span data-ttu-id="612d6-115">Pour plus d’informations sur les contraintes de bande passante pour les médias, voir [besoins en bande passante réseau pour le trafic multimédia dans Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="612d6-115">For details about media bandwidth requirements, see [Network bandwidth requirements for media traffic in Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span></span>

<span data-ttu-id="612d6-116">Si vous déployez la conférence audio sur votre réseau, vos utilisateurs auront besoin de périphériques audio, comme des casques pour y participer.</span><span class="sxs-lookup"><span data-stu-id="612d6-116">If you deploy audio conferencing in your network, your users will need audio devices such as headsets to participate in an audio conference.</span></span> <span data-ttu-id="612d6-117">Si vous déployez la conférence vidéo, vous devez déployer des périphériques vidéo, comme des webcams pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="612d6-117">If you deploy video conferencing, you need to deploy video devices, such as webcams for users.</span></span> <span data-ttu-id="612d6-118">Nous vous recommandons d’utiliser des appareils de communications unifiées (UC) certifiés par Microsoft pour tous les types d’appareils, afin de garantir une utilisation optimale des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="612d6-118">We recommend that you use unified communications (UC) devices that are certified by Microsoft for all device types, to ensure an optimal user experience.</span></span> <span data-ttu-id="612d6-119">Pour plus d’informations sur les appareils validés par UC, voir « téléphones et appareils pour Lync » à l’adresse [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861) .</span><span class="sxs-lookup"><span data-stu-id="612d6-119">For details about UC-certified devices, see "Phones and Devices for Lync" at [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861).</span></span> <span data-ttu-id="612d6-120">Pour les périphériques audio ou vidéo, le déploiement de périphériques et la formation des utilisateurs, vous devez prendre en compte les étapes à suivre.</span><span class="sxs-lookup"><span data-stu-id="612d6-120">For either audio or video devices, device deployment, and user training are important steps for you to consider and plan for.</span></span>

<span data-ttu-id="612d6-121">Les sections suivantes décrivent les fonctionnalités des conférences audio et vidéo, ainsi que des informations sur la gestion de la bande passante et la sélection des clients appropriés.</span><span class="sxs-lookup"><span data-stu-id="612d6-121">The following sections describe the features for audio and video conferencing, including information about managing bandwidth and selecting the appropriate clients.</span></span>

<div>

## <a name="audio-conferencing-features"></a><span data-ttu-id="612d6-122">Fonctionnalités de l’audioconférence</span><span class="sxs-lookup"><span data-stu-id="612d6-122">Audio Conferencing Features</span></span>

<span data-ttu-id="612d6-123">Lync Server 2013 fournit plusieurs fonctionnalités que vous pouvez utiliser pour configurer l’interface de visioconférence pour l’utilisateur, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="612d6-123">Lync Server 2013 provides several features that you can use to configure the audio conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="612d6-124">**Désactiver**   le son pour les participants   Le présentateur peut utiliser ce paramètre pour désactiver le son de tous les participants audio de la Conférence et mettre la Conférence dans un État où les non-présentateurs ne peuvent pas le désactiver.</span><span class="sxs-lookup"><span data-stu-id="612d6-124">**Audience mute**   The presenter can use this setting to mute all the audio participants in the conference and put the conference in a state where non-presenters cannot unmute themselves.</span></span>

  - <span data-ttu-id="612d6-125">**Annonces d’entrée/de sortie de conférence**   Si vous avez activé la fonction de conférence rendez-vous, les présentateurs peuvent utiliser ce paramètre pour activer ou désactiver les annonces d’entrée et de sortie afin de réduire le risque de distraction lors de l’exécution d’une conférence.</span><span class="sxs-lookup"><span data-stu-id="612d6-125">**Conferencing Entry/Exit Announcements**   If you have enabled dial-in conferencing, presenters can use this setting to turn entry and exit announcements on or off to minimize distractions while a conference is in progress.</span></span>

  - <span data-ttu-id="612d6-126">**Ajouter un utilisateur en composant un numéro de téléphone**   Les présentateurs et les participants qui ont reçu une autorisation peuvent ajouter des numéros RTC aux conférences et être disposant d’une conférence rendez-vous pour ces numéros.</span><span class="sxs-lookup"><span data-stu-id="612d6-126">**Adding a user by dialing out**   Presenters and attendees that have been given permission, can add PSTN numbers to the conferences and have the conference dial-out to those numbers.</span></span>

</div>

<div>

## <a name="video-conferencing-features"></a><span data-ttu-id="612d6-127">Fonctionnalités de conférence vidéo</span><span class="sxs-lookup"><span data-stu-id="612d6-127">Video Conferencing Features</span></span>

<span data-ttu-id="612d6-128">Lync Server 2013 fournit plusieurs fonctionnalités que vous pouvez utiliser pour configurer l’interface de conférence vidéo pour l’utilisateur, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="612d6-128">Lync Server 2013 provides several features that you can use to configure the video conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="612d6-129">**Affichage Galerie**   Dans les conférences vidéo ayant plus de deux personnes, les utilisateurs voient automatiquement tous les participants à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="612d6-129">**Gallery View**   In video conferences that have more than two people, users automatically see everyone in the conference.</span></span> <span data-ttu-id="612d6-130">Si la conférence rassemble plus de cinq participants, la vidéo des participants les plus actifs s’affiche sur la ligne supérieure et seule la photo s’affiche pour les autres participants.</span><span class="sxs-lookup"><span data-stu-id="612d6-130">If the conference has more than five participants, the video of the most active participants appear in the top row and only the photo appears for the other participants.</span></span> <span data-ttu-id="612d6-131">La vidéo à plusieurs est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="612d6-131">Multiparty video is turned on by default.</span></span> <span data-ttu-id="612d6-132">Pour plus d’informations sur la configuration ou la désactivation de la vidéo à plusieurs parties, voir [configuration de la bande passante vidéo dans Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span><span class="sxs-lookup"><span data-stu-id="612d6-132">For details about configuring or turning off multiparty video, see [Configuring video bandwidth in Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span></span>

  - <span data-ttu-id="612d6-133">**Vidéo panoramique**   Si un appareil de visioconférence vidéo RoundTable est installé dans la salle de conférence, cette fonctionnalité fournit une vue complète de 360 degrés de la salle de conférence.</span><span class="sxs-lookup"><span data-stu-id="612d6-133">**Panoramic Video**   If a RoundTable video conferencing device is installed in the conferencing room, this feature provides a full 360 degree view of the conference room.</span></span> <span data-ttu-id="612d6-134">Le clip vidéo panoramique n’est disponible qu’avec les appareils RoundTable.</span><span class="sxs-lookup"><span data-stu-id="612d6-134">The panoramic video strip is only available with RoundTable devices.</span></span>

  - <span data-ttu-id="612d6-135">**Mode vidéo du présentateur uniquement**   Les présentateurs peuvent configurer la réunion de façon à ce que seule la vidéo du présentateur soit affichée.</span><span class="sxs-lookup"><span data-stu-id="612d6-135">**Presenter only video mode**   Presenters can configure the meeting so that only the video from the presenter is shown.</span></span> <span data-ttu-id="612d6-136">Cela empêche toute distraction lors de grandes réunions, lorsque plusieurs flux vidéo sont disponibles et verrouillés à différentes sources.</span><span class="sxs-lookup"><span data-stu-id="612d6-136">This prevents distractions in large meetings when multiple video streams are available and locking to different sources.</span></span> <span data-ttu-id="612d6-137">Ce mode s’applique également à la vidéo capturée et fournie par les appareils RoundTable.</span><span class="sxs-lookup"><span data-stu-id="612d6-137">This mode also applies to video captured and provided by RoundTable devices.</span></span>

  - <span data-ttu-id="612d6-138">**Vidéo HD**   Les utilisateurs peuvent bénéficier de résolutions allant jusqu’à HD 1080P dans les appels et conférences à deux parties.</span><span class="sxs-lookup"><span data-stu-id="612d6-138">**HD video**   Users can experience resolutions up to HD 1080P in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="612d6-139">**Actualités vidéo**   Les présentateurs peuvent configurer la réunion de telle sorte que seule la vidéo d’un participant sélectionné qui est une source vidéo est visible par les autres participants à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="612d6-139">**Video Spotlight**   Presenters can configure the meeting so that only the video from a selected participant who is a video source is seen by the other participants in the conference.</span></span> <span data-ttu-id="612d6-140">Ce mode s’applique également à la vidéo capturée et fournie par les appareils RoundTable pour la vidéo panoramique.</span><span class="sxs-lookup"><span data-stu-id="612d6-140">This mode also applies to video captured and provided by RoundTable devices for panoramic video.</span></span>

<span data-ttu-id="612d6-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="612d6-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

