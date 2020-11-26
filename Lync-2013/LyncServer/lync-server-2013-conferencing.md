---
title: Conférence Lync Server 2013
description: Lync Server 2013 Conferencing.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing
ms:assetid: 6129b7e0-9abd-488e-a54e-86094eb9df7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417161(v=OCS.15)
ms:contentKeyID: 48184274
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d4a5f1ca1edc6246aace56c8a4bfa5b5215c4bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434255"
---
# <a name="conferencing-in-lync-server-2013"></a><span data-ttu-id="202c0-103">Conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="202c0-103">Conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="202c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="202c0-104">

<span> </span></span></span>

<span data-ttu-id="202c0-105">_**Dernière modification de la rubrique :** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="202c0-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="202c0-106">Grâce à la Conférence unifiée dans Lync Server 2013, les utilisateurs peuvent collaborer, partager des informations et coordonner leurs efforts en temps réel.</span><span class="sxs-lookup"><span data-stu-id="202c0-106">With unified conferencing in Lync Server 2013, users can collaborate, share information, and coordinate their efforts in real time.</span></span> <span data-ttu-id="202c0-107">Tous vos utilisateurs peuvent utiliser la totalité de la collaboration, des réunions planifiées et des outils de réunion involontaires.</span><span class="sxs-lookup"><span data-stu-id="202c0-107">All your users can use the full breadth of spontaneous collaboration, scheduled meetings, and meeting tools.</span></span> <span data-ttu-id="202c0-108">Les fonctionnalités de visioconférence et de visioconférence peuvent être utilisées à partir de n’importe quel emplacement disposant d’une connexion Internet, et les utilisateurs en dehors d’un ordinateur peuvent participer à des conférences audio en se connectant à l’aide d’un téléphone RTC (réseau téléphonique commuté).</span><span class="sxs-lookup"><span data-stu-id="202c0-108">Voice and video conferencing capabilities can be used from any location with an Internet connection, and users away from a computer can participate in audio conferences by dialing in with a public switched telephone network (PSTN) phone.</span></span>

<span data-ttu-id="202c0-109">Les outils de réunion intégrés dans Outlook permettent aux organisateurs de planifier une réunion ou de lancer une conférence impromptue en un seul clic, et de la rendre aussi simple aux participants.</span><span class="sxs-lookup"><span data-stu-id="202c0-109">Meeting tools integrated into Outlook enable organizers to schedule a meeting or start an impromptu conference with a single click, and also make it just as easy for attendees to join.</span></span> <span data-ttu-id="202c0-110">Un client Web étend les fonctionnalités de conférence riches aux participants qui n’exécutent pas la version de bureau de Lync.</span><span class="sxs-lookup"><span data-stu-id="202c0-110">A web client extends rich conference features to participants who are not running the desktop version of Lync.</span></span>

<div>

## <a name="audio-and-video-conferencing"></a><span data-ttu-id="202c0-111">Conférence audio et vidéo</span><span class="sxs-lookup"><span data-stu-id="202c0-111">Audio and Video Conferencing</span></span>

<span data-ttu-id="202c0-112">Lync Server fournit une expérience utilisateur familière aux utilisateurs de services audio Bridge traditionnels, y compris les services RTC Dial-in avec des commandes de contrôle d’appel à tonalité.</span><span class="sxs-lookup"><span data-stu-id="202c0-112">Lync Server provides a user experience that is familiar to users of traditional audio bridge services including PSTN dial-in services with touch-tone call control commands.</span></span> <span data-ttu-id="202c0-113">En même temps, elle intègre des fonctionnalités de planification, de jointure et de gestion puissantes disponibles uniquement avec une plate-forme de communications unifiées intégrée.</span><span class="sxs-lookup"><span data-stu-id="202c0-113">At the same time, it incorporates powerful scheduling, joining, and management features available only with an integrated unified communications platform.</span></span>

<span data-ttu-id="202c0-114">D’un simple clic, les utilisateurs peuvent planifier une réunion à partir d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="202c0-114">With a single click, users can schedule a meeting from Outlook.</span></span> <span data-ttu-id="202c0-115">Les détails, tels que l’heure de la réunion, l’emplacement et les participants, suivent le modèle Outlook familier.</span><span class="sxs-lookup"><span data-stu-id="202c0-115">Details, such as meeting time, location, and attendees, follow the familiar Outlook template.</span></span> <span data-ttu-id="202c0-116">De plus, les informations spécifiques aux conférences téléphoniques, telles que le numéro de connexion, les ID de réunion et les rappels de code confidentiel, sont automatiquement renseignées.</span><span class="sxs-lookup"><span data-stu-id="202c0-116">Additionally, conference call-specific information, such as dial-in number, meeting IDs, and personal identification number (PIN) reminders, are automatically populated.</span></span>

<span data-ttu-id="202c0-117">Pour garantir que seules les personnes autorisées participent à un appel, Lync Server fournit plusieurs niveaux d’authentification pour les participants.</span><span class="sxs-lookup"><span data-stu-id="202c0-117">To help ensure that only the authorized people participate in a call, Lync Server provides multiple levels of authentication for participants.</span></span> <span data-ttu-id="202c0-118">Les utilisateurs qui se connectent à l’aide de Lync sont déjà authentifiés par les services de domaine Active Directory et n’ont pas besoin d’entrer un code confidentiel, un code de passage ou un ID de réunion.</span><span class="sxs-lookup"><span data-stu-id="202c0-118">Users who join by using Lync are already authenticated by the Active Directory Domain Services and do not need to enter a PIN, pass code, or meeting ID.</span></span>

<span data-ttu-id="202c0-119">Lync simplifie l’utilisation de l’utilisateur pour les conférences vidéo en incorporant la vidéo dans le client unifié, de sorte que la planification d’une réunion avec des vidéos ou la réutilisation de la vidéo est transparente et facile.</span><span class="sxs-lookup"><span data-stu-id="202c0-119">Lync simplifies the video conferencing user experience by incorporating video into the unified client so that scheduling a meeting with video or escalating to video spontaneously is seamless and easy.</span></span>

<span data-ttu-id="202c0-120">Lync Server vous permet d’ajouter facilement une vidéo à un appel téléphonique standard en un seul clic.</span><span class="sxs-lookup"><span data-stu-id="202c0-120">Lync Server makes it easy to add video to a standard phone call in just one click.</span></span> <span data-ttu-id="202c0-121">Lorsqu’un appel vidéo ou une conférence est en plusieurs participants, chaque utilisateur peut voir la vidéo d’un maximum de cinq utilisateurs simultanément, ou un présentateur peut choisir une seule source vidéo à afficher en exclusivité par tout le monde.</span><span class="sxs-lookup"><span data-stu-id="202c0-121">When there are multiple participants in a video call or a conference, each user can see video from up to five other users simultaneously, or a presenter can choose just one video source to be seen exclusively by everyone.</span></span>

<span data-ttu-id="202c0-122">Vidéo haute définition (résolution 1270 x 720 ; rapport hauteur/largeur 16:9) et vidéo VGA (résolution 640 x 480 ; rapport hauteur/largeur 4:3) prises en charge pour les appels d’égal à égal entre les utilisateurs exécutant Lync sur des ordinateurs haut de gamme.</span><span class="sxs-lookup"><span data-stu-id="202c0-122">High-definition video (resolution 1270 x 720; aspect ratio 16:9) and VGA video (resolution 640 x 480; aspect ratio 4:3) are supported for peer-to-peer calls between users running Lync on high-end computers.</span></span> <span data-ttu-id="202c0-123">La résolution affichée par chaque participant pour une seule conversation peut varier en fonction des capacités vidéo du matériel respectif de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="202c0-123">The resolution viewed by each participant in a single conversation may differ, depending on the video capabilities of each user’s respective hardware.</span></span>

<span data-ttu-id="202c0-124">Les administrateurs informatiques peuvent définir des stratégies permettant de limiter ou de désactiver la vidéo haute définition ou VGA sur des clients, en fonction de la fonctionnalité de votre ordinateur, de la bande passante du réseau et de la présence d’une caméra capable de répondre à la résolution requise.</span><span class="sxs-lookup"><span data-stu-id="202c0-124">IT administrators can set policies to restrict or disable high-definition or VGA video on clients, depending on computer capability, network bandwidth, and the presence of a camera able to deliver the required resolution.</span></span> <span data-ttu-id="202c0-125">Ces stratégies sont appliquées par le biais de la mise en service intrabande.</span><span class="sxs-lookup"><span data-stu-id="202c0-125">These policies are enforced through in-band provisioning.</span></span>

</div>

<div>

## <a name="web-conferencing"></a><span data-ttu-id="202c0-126">Conférence web</span><span class="sxs-lookup"><span data-stu-id="202c0-126">Web conferencing</span></span>

<span data-ttu-id="202c0-127">Lync Server intègre des fonctionnalités de partage de conférences telles que l’ordinateur de bureau, l’application, la pièce jointe, le tableau blanc, le sondage et PowerPoint dans le Lync rationalisé.</span><span class="sxs-lookup"><span data-stu-id="202c0-127">Lync Server integrates conferencing sharing features such as desktop, application, attachment, whiteboard, poll and PowerPoint into the streamlined Lync.</span></span> <span data-ttu-id="202c0-128">Combinés à des conférences audio ou vidéo, le résultat est une session de collaboration et de collaboration plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="202c0-128">Combined with audio or video conferencing, the result is a highly immersive and collaborative session that is simple to facilitate.</span></span>

<span data-ttu-id="202c0-129">Pour améliorer l’utilisation globale des utilisateurs qui présentent ou visualisent des présentations PowerPoint, Lync Server 2013 utilise Office Web Apps pour gérer des présentations PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="202c0-129">To improve the overall experience of users presenting or viewing PowerPoint presentations, Lync Server 2013 employs Office Web Apps to handle PowerPoint presentations.</span></span> <span data-ttu-id="202c0-130">Les utilisateurs peuvent partager une image ou copier et coller du texte à l’aide d’un tableau blanc dans une réunion Lync.</span><span class="sxs-lookup"><span data-stu-id="202c0-130">Users can share a picture or copy and paste text using a Whiteboard in the Lync meeting.</span></span> <span data-ttu-id="202c0-131">Les présentateurs peuvent organiser des sondages au sein de la réunion Lync afin de solliciter des commentaires des participants.</span><span class="sxs-lookup"><span data-stu-id="202c0-131">Presenters can conduct polls in the Lync meeting to solicit feedback from the attendees.</span></span>

<span data-ttu-id="202c0-132">Le partage de bureau permet aux présentateurs de diffuser tout visuel, application, page Web, document, logiciel ou partie de leur bureau à des participants distants en temps réel, directement à partir de Lync.</span><span class="sxs-lookup"><span data-stu-id="202c0-132">Desktop sharing enables presenters to broadcast any visuals, applications, webpages, documents, software, or part of their desktops to remote participants in real time, right from Lync.</span></span> <span data-ttu-id="202c0-133">Les membres de l’assistance peuvent suivre les mouvements de la souris et le clavier.</span><span class="sxs-lookup"><span data-stu-id="202c0-133">Audience members can follow along with mouse movements and keyboard input.</span></span> <span data-ttu-id="202c0-134">Les présentateurs peuvent choisir de partager tout l’écran ou seulement une partie.</span><span class="sxs-lookup"><span data-stu-id="202c0-134">Presenters can choose to share the entire screen or only a portion.</span></span> <span data-ttu-id="202c0-135">En partageant leurs bureaux, les présentateurs sont en mesure de s’impliquer sur leur public dans les démonstrations de produit ou logiciels interactifs depuis n’importe où.</span><span class="sxs-lookup"><span data-stu-id="202c0-135">By sharing their desktops, presenters are able to engage with their audiences in interactive product or software demos from any location.</span></span>

<span data-ttu-id="202c0-136">Le partage d’application permet aux présentateurs de partager le contrôle des logiciels sur leur ordinateur de bureau, sans perte d’affichage des commentaires ou des questions relatives aux participants.</span><span class="sxs-lookup"><span data-stu-id="202c0-136">Application sharing enables presenters to share control of software on their desktops without losing sight of participant feedback or text questions.</span></span> <span data-ttu-id="202c0-137">Les présentateurs peuvent également déléguer le contrôle de l’application aux participants à la réunion.</span><span class="sxs-lookup"><span data-stu-id="202c0-137">Presenters can also delegate control of the application to meeting participants.</span></span>

</div>

<div>

## <a name="dial-in-conferencing"></a><span data-ttu-id="202c0-138">Conférence rendez-vous</span><span class="sxs-lookup"><span data-stu-id="202c0-138">Dial-in Conferencing</span></span>

<span data-ttu-id="202c0-139">Pour les utilisateurs qui n’utilisent pas d’ordinateur personnel, il existe plusieurs méthodes pour participer à une téléconférence Lync Server.</span><span class="sxs-lookup"><span data-stu-id="202c0-139">For users that are not using a personal computer, there are several methods available for joining a Lync Server conference call.</span></span> <span data-ttu-id="202c0-140">Un utilisateur RTC peut composer un numéro d’accès, accéder au pont de réunion, puis entrer l’ID de la réunion.</span><span class="sxs-lookup"><span data-stu-id="202c0-140">A PSTN user can dial an access number, access the meeting bridge, and then enter the meeting ID.</span></span> <span data-ttu-id="202c0-141">Pour des réunions plus sûres, l’utilisateur peut également être tenu d’entrer son code confidentiel pour s’authentifier auprès d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="202c0-141">For more secure meetings, the user can also be required to enter his or her PIN to authenticate against Active Directory.</span></span> <span data-ttu-id="202c0-142">Lync Server prend également en charge les appareils Lync Phone Edition, qui sont des appareils de téléphone IP autonomes proposés par des partenaires Microsoft.</span><span class="sxs-lookup"><span data-stu-id="202c0-142">Lync Server also supports Lync Phone Edition devices, which are stand-alone IP phone devices provided by Microsoft partners.</span></span>

<span data-ttu-id="202c0-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="202c0-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

