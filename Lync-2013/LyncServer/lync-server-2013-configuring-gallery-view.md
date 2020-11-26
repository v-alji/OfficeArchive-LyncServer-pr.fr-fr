---
title: 'Lync Server 2013 : configuration de l’affichage Galerie'
description: 'Lync Server 2013 : configuration de l’affichage Galerie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Gallery View
ms:assetid: 4a609178-47d8-4682-ac8d-29f882801924
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204871(v=OCS.15)
ms:contentKeyID: 48184069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2aec2f1e3c7bff9a3736f40584a29880978b9daa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433093"
---
# <a name="configuring-gallery-view-in-lync-server-2013"></a><span data-ttu-id="9cfcf-103">Configurer le mode Galerie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9cfcf-103">Configuring Gallery View in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9cfcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9cfcf-104">

<span> </span></span></span>

<span data-ttu-id="9cfcf-105">_**Dernière modification de la rubrique :** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="9cfcf-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="9cfcf-106">Dans Lync Server 2013, vous configurez la conférence vidéo d’affichage de la galerie dans la stratégie de conférence.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-106">In Lync Server 2013, you configure Gallery View video conferencing in conferencing policy.</span></span> <span data-ttu-id="9cfcf-107">L’option vue Galerie est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-107">Gallery View is turned on by default.</span></span> <span data-ttu-id="9cfcf-108">Si vous ne voulez pas autoriser le mode Galerie, ou si vous voulez l’autoriser pour certains utilisateurs, vous devez désactiver la fonctionnalité dans la stratégie de conférence.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-108">If you do not want to allow Gallery View, or want to allow it for only some users, you need to turn off the feature in conferencing policy.</span></span>

<span data-ttu-id="9cfcf-109">Lorsque la vidéo d’un participant à la Conférence n’est pas disponible, il est possible d’améliorer l’affichage de la Galerie de la Galerie des utilisateurs si vous déployez des photos haute résolution, une nouvelle fonctionnalité dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-109">When a conference participant's video is not available, the users' Gallery View experience can be enhanced if you deploy high-resolution photos, a new feature in Lync Server 2013.</span></span> <span data-ttu-id="9cfcf-110">Les photos haute résolution constituent une alternative aux photos de contact plus petites et limitées stockées dans les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="9cfcf-110">High-resolution photos provide an alternative to the smaller, limited resolution contact photos stored in Active Directory Domain Services.</span></span> <span data-ttu-id="9cfcf-111">Les photos haute résolution sont stockées dans la boîte aux lettres Exchange 2013 d’un utilisateur et nécessitent donc l’intégration de Lync Server 2013 avec Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-111">High-resolution photos are stored in a user's Exchange 2013 mailbox, and, therefore, require you to integrate Lync Server 2013 with Exchange 2013.</span></span> <span data-ttu-id="9cfcf-112">Pour plus d’informations, consultez l’article de blog NextHop intitulé « intégration d’Exchange 2013 et Lync Server 2013 » [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987) .</span><span class="sxs-lookup"><span data-stu-id="9cfcf-112">For details, see the NextHop blog article, "Integrating Exchange 2013 and Lync Server 2013," at [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9cfcf-113">Le contenu des blogs et leurs URL peuvent être modifiés sans préavis.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-113">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

<span data-ttu-id="9cfcf-114">Vous pouvez afficher ou modifier les paramètres d’affichage de la galerie en utilisant le panneau de configuration de Lync Server 2013 ou en utilisant l’une des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cfcf-114">You can view or modify the Gallery View parameters by using Lync Server 2013 Control Panel or by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="9cfcf-115">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="9cfcf-115">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="9cfcf-116">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="9cfcf-116">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="9cfcf-117">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="9cfcf-117">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="9cfcf-118">Configurer le mode Galerie avec les paramètres de stratégie de conférence suivants :</span><span class="sxs-lookup"><span data-stu-id="9cfcf-118">Configure Gallery View with the following conferencing policy settings:</span></span>

  - <span data-ttu-id="9cfcf-119">**AllowMultiview**   Ce paramètre indique si un utilisateur est autorisé à organiser des conférences vidéo d’affichage Galerie.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-119">**AllowMultiview**   This parameter controls whether a user is allowed to organize Gallery View video conferences.</span></span> <span data-ttu-id="9cfcf-120">Ce paramètre s’applique aux réunions planifiées et ponctuelles créées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-120">This parameter applies to scheduled and ad-hoc meetings created by the user.</span></span>
    
    <span data-ttu-id="9cfcf-121">Donnés</span><span class="sxs-lookup"><span data-stu-id="9cfcf-121">Examples:</span></span>
    
      - <span data-ttu-id="9cfcf-122">Ce paramètre est défini sur true pour l’utilisateur A qui est hébergé sur un pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-122">This parameter is set to True for User A, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="9cfcf-123">Réunions organisées par l’utilisateur permet aux utilisateurs de joindre et de recevoir plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-123">Meetings organized by User A enable users to join and receive multiple video streams.</span></span>
    
      - <span data-ttu-id="9cfcf-124">Ce paramètre est défini sur false pour l’utilisateur B, qui est hébergé sur un pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-124">This parameter is set to False for User B, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="9cfcf-125">Les réunions organisées par l’utilisateur B sont dotées d’un flux vidéo unique qui est semblable à l’interface de visioconférence fournie par Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-125">Meetings organized by User B have a single video stream that is similar to the video conference experience provided by Lync Server 2010.</span></span>
    
    <span data-ttu-id="9cfcf-126">Ce paramètre détermine qui peut organiser des réunions qui autorisent plusieurs flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-126">This parameter determines who can organize meetings that allow multiple video streams.</span></span> <span data-ttu-id="9cfcf-127">Les participants à des réunions qui autorisent plusieurs flux vidéo peuvent, ou ne peuvent pas être autorisés à recevoir plusieurs flux vidéo, en fonction de leurs autorisations individuelles (voir la description du paramètre EnableMultiviewJoin).</span><span class="sxs-lookup"><span data-stu-id="9cfcf-127">Participants in meetings that allow multiple video streams may or may not be allowed to receive multiple video streams, based on their individual permissions (see the description for the EnableMultiviewJoin parameter).</span></span>

  - <span data-ttu-id="9cfcf-128">**EnableMultiviewJoin**   Ce paramètre détermine si un participant à une réunion reçoit l’interface vidéo d’affichage de la galerie dans les réunions qui le permettent.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-128">**EnableMultiviewJoin**   This parameter controls whether a participant in a meeting receives the Gallery View video experience in meetings that allow it.</span></span> <span data-ttu-id="9cfcf-129">Ce paramètre contrôle l’utilisation de l’utilisateur dans les réunions auxquelles il participe.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-129">This parameter controls the user's experience in any meeting in which he or she participates.</span></span>
    
    <span data-ttu-id="9cfcf-130">Donnés</span><span class="sxs-lookup"><span data-stu-id="9cfcf-130">Examples:</span></span>
    
      - <span data-ttu-id="9cfcf-131">Ce paramètre est défini sur true pour l’utilisateur C. l’utilisateur c peut recevoir plusieurs flux vidéo lorsque vous participez à une réunion organisée ou démarrée par l’utilisateur A. l’utilisateur dispose d’un flux vidéo unique similaire à l’interface de visioconférence fournie 2010 par l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-131">This parameter is set to True for User C. User C can receive multiple video streams when participating in a meeting organized or started by User A. User C receives a single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in a meeting organized or started by User B.</span></span>
    
      - <span data-ttu-id="9cfcf-132">Ce paramètre est défini sur false pour l’utilisateur D. User d reçoit un flux vidéo unique qui est semblable à l’interface de visioconférence fournie par Lync Server 2010 lors de la participation à une réunion organisée par l’utilisateur A ou par l’utilisateur B.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-132">This parameter is set to False for User D. User D receives single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in any meeting organized by User A or User B.</span></span>

<span data-ttu-id="9cfcf-133">Vous trouverez ci-dessous un exemple d’utilisation de Lync Server Management Shell pour activer la vidéoconférence d’affichage Galerie.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-133">The following procedure is an example of using Lync Server Management Shell to enable Gallery View video conferencing.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-gallery-view-video-conferencing"></a><span data-ttu-id="9cfcf-134">Pour modifier la stratégie de conférence pour les conférences vidéo sur l’affichage Galerie</span><span class="sxs-lookup"><span data-stu-id="9cfcf-134">To modify conferencing policy for Gallery View video conferencing</span></span>

1.  <span data-ttu-id="9cfcf-135">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="9cfcf-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="9cfcf-136">Dans la ligne de commande, exécutez l’applet de commande suivante pour modifier la stratégie de conférence :</span><span class="sxs-lookup"><span data-stu-id="9cfcf-136">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -AllowMultiview $true -EnableMultiviewJoin $true 

<span data-ttu-id="9cfcf-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9cfcf-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

