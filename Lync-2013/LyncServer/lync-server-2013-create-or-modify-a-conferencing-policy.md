---
title: 'Lync Server 2013 : création ou modification d’une stratégie de conférence'
description: 'Lync Server 2013 : création ou modification d’une stratégie de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing policy
ms:assetid: e2974030-2c0a-4634-91e8-93f4e2d674d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721910(v=OCS.15)
ms:contentKeyID: 49733844
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8715dcde033c4181069f3e30f65b3c29231f51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394376"
---
# <a name="create-or-modify-a-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="7a4ba-103">Création ou modification d’une stratégie de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a4ba-103">Create or modify a conferencing policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a4ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a4ba-104">

<span> </span></span></span>

<span data-ttu-id="7a4ba-105">_**Dernière modification de la rubrique :** 2013-02-07_</span><span class="sxs-lookup"><span data-stu-id="7a4ba-105">_**Topic Last Modified:** 2013-02-07_</span></span>

<span data-ttu-id="7a4ba-106">Procédez comme suit pour créer une stratégie de niveau utilisateur ou de niveau site.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-106">Follow these steps to create a user-level or a site-level conferencing policy.</span></span> <span data-ttu-id="7a4ba-107">Pour plus d’informations sur l’affectation d’une stratégie de niveau utilisateur à un utilisateur, voir [affecter une stratégie de conférence par utilisateur dans Lync Server 2013](lync-server-2013-assign-a-per-user-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-107">For details about how to assign a user-level policy to a user, see [Assign a per-user conferencing policy in Lync Server 2013](lync-server-2013-assign-a-per-user-conferencing-policy.md).</span></span> <span data-ttu-id="7a4ba-108">Pour obtenir la liste de tous les paramètres de stratégie de conférence disponibles, voir [référence des paramètres de stratégie de conférence pour Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-108">For a list of all available conferencing policy settings, see [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<div>

## <a name="to-create-a-new-user-or-site-policy"></a><span data-ttu-id="7a4ba-109">Pour créer une nouvelle stratégie d’utilisateur ou de site</span><span class="sxs-lookup"><span data-stu-id="7a4ba-109">To create a new user or site policy</span></span>

1.  <span data-ttu-id="7a4ba-110">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7a4ba-111">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7a4ba-112">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7a4ba-113">Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur **stratégie de conférence**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-113">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="7a4ba-114">Cliquez sur **Nouveau**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-114">Click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-p103">Pour créer une stratégie au niveau de l’utilisateur, cliquez sur **Stratégie utilisateur**. Dans **Nouvelle stratégie de conférence**, dans **Nom**, tapez un nom descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p103">To create a user-level policy, click **User policy**. In **New Conferencing Policy**, in **Name**, type a descriptive name for the policy.</span></span>
    
      - <span data-ttu-id="7a4ba-p104">Pour créer une stratégie au niveau site, cliquez sur **Stratégie de site**. Dans la zone de recherche **Sélectionner un site**, tapez entièrement ou partiellement le nom du site pour lequel vous voulez créer une stratégie. Dans la liste des sites, cliquez sur le site voulu, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p104">To create a site-level policy, click **Site policy**. In the **Select a Site** search field, type all or part of the name of the site for which you want to create a policy. In the list of sites, click the site that you want, and then click **OK**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="7a4ba-120">Le nom du site devient le nom de la stratégie de conférence et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-120">The site name becomes the conferencing policy name, and it cannot be changed.</span></span>

        
        </div>

5.  <span data-ttu-id="7a4ba-121">Dans **Description**, tapez la description de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-121">In **Description**, type a description for the policy.</span></span>

6.  <span data-ttu-id="7a4ba-p105">Sous **Stratégie de l’organisateur**, dans **Taille maximale de la réunion**, tapez le nombre maximal d’utilisateurs autorisés à participer à une réunion. Par défaut, la taille maximale de la réunion est définie sur 250.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p105">Under **Organizer policy**, in **Maximum meeting size**, type the maximum number of users that you want to allow at a meeting. By default, the maximum meeting size is 250.</span></span>

7.  <span data-ttu-id="7a4ba-124">Pour empêcher les utilisateurs d’inviter des utilisateurs anonymes aux réunions, désactivez la case à cocher **Autoriser les participants à inviter des utilisateurs anonymes**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-124">To prevent users from inviting anonymous users to meetings, clear the **Allow participants to invite anonymous users** check box.</span></span> <span data-ttu-id="7a4ba-125">Les utilisateurs anonymes sont des utilisateurs qui ne disposent pas des informations d’identification dans les services de domaine Active Directory de votre organisation et qui, par conséquent, ne sont pas authentifiés.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-125">Anonymous users are users who do not have credentials in your organization’s Active Directory Domain Services and who, therefore, are not authenticated.</span></span> <span data-ttu-id="7a4ba-126">Par défaut, les utilisateurs peuvent inviter des utilisateurs anonymes aux réunions.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-126">By default, users can invite anonymous users to meetings.</span></span>

8.  <span data-ttu-id="7a4ba-127">Dans **Enregistrement**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-127">In **Recording**, do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-p107">Pour interdire aux participants d’enregistrer les réunions, cliquez sur **Aucun**. Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p107">To prevent participants from recording meetings, click **None**. This is the default setting.</span></span>
    
      - <span data-ttu-id="7a4ba-130">Pour autoriser les participants à enregistrer les réunions, cliquez sur **Activer l’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-130">To allow participants to record meetings, click **Enable recording**.</span></span>

9.  <span data-ttu-id="7a4ba-p108">Pour autoriser les participants externes à enregistrer les réunions, activez la case à cocher **Autoriser les participants fédérés et anonymes à enregistrer**. Par défaut, le système interdit aux participants externes d’enregistrer les réunions.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p108">To allow external participants to record meetings, select the **Allow federated and anonymous participants to record** check box. The default is to prevent external participants from recording meetings.</span></span>

10. <span data-ttu-id="7a4ba-133">Dans **Audio/vidéo**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-133">In **Audio/video**, do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-134">Pour interdire l’utilisation de l’audio et de la vidéo, cliquez sur **Aucun**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-134">To prevent the use of audio and video, click **None**.</span></span>
    
      - <span data-ttu-id="7a4ba-135">Pour autoriser l’utilisation de l’audio mais pas de la vidéo, cliquez sur **Activer Audio sur IP**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-135">To allow the use of audio but not video, click **Enable IP audio**.</span></span>
    
      - <span data-ttu-id="7a4ba-p109">Pour autoriser l’utilisation de l’audio et de la vidéo, cliquez sur **Activer l’audio/la vidéo IP**. Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p109">To allow the use of audio and video, click **Enable IP audio/video**. This is the default setting.</span></span>

11. <span data-ttu-id="7a4ba-138">Si vous avez choisi d’autoriser l’utilisation de l’audio dans **Audio/vidéo**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-138">If you chose to allow the use of audio in **Audio/video**, do the following:</span></span>
    
      - <span data-ttu-id="7a4ba-p110">Pour empêcher les utilisateurs de rejoindre la réunion via un appel à distance, désactivez la case à cocher **Activer la conférence rendez-vous RTC**. Par défaut, les utilisateurs peuvent accéder aux réunions par le biais du réseau téléphonique commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p110">To prevent users from joining the meeting by dialing in, clear the **Enable PSTN dial-in conferencing** check box. By default, users can dial in to meetings by using the public switched telephone network (PSTN).</span></span>
    
      - <span data-ttu-id="7a4ba-p111">Si vous autorisez les utilisateurs à accéder aux réunions à distance et que vous souhaitez autoriser les utilisateurs non authentifiés (anonymes) à rejoindre une réunion via un appel téléphonique sortant, activez la case à cocher **Autoriser l’accès sortant des participants anonymes**. Avec l’appel téléphonique sortant, le serveur de conférence appelle l’utilisateur et celui-ci répond au téléphone pour rejoindre la réunion. Par défaut, les utilisateurs anonymes ne peuvent pas rejoindre une réunion via un appel téléphonique sortant.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p111">If you allow users to dial in to meetings and you want to allow unauthenticated (anonymous) users to join a meeting by using dial out phoning, select the **Allow anonymous participants to dial out** check box. With dial-out phoning, the conference server calls the user, and the user answers the phone to join the meeting. By default, anonymous users cannot join a meeting by using dial-out phoning.</span></span>

12. <span data-ttu-id="7a4ba-144">Si vous choisissez d’autoriser l’utilisation de la vidéo dans les **fichiers audio/vidéo**, activez la case à cocher **autoriser plusieurs flux vidéo** .</span><span class="sxs-lookup"><span data-stu-id="7a4ba-144">If you chose to allow the use of video in **Audio/video**, check **Allow multiple video streams** .</span></span>

13. <span data-ttu-id="7a4ba-145">Dans **Collaboration de données**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-145">In **Data collaboration**, do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-146">Pour empêcher la collaboration de données, cliquez sur **Aucun**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-146">To prevent data collaboration, click **None**.</span></span>
    
      - <span data-ttu-id="7a4ba-p112">Pour autoriser la collaboration de données, cliquez sur **Activer la collaboration de données**. Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p112">To allow data collaboration, click **Enable data collaboration**. This is the default setting.</span></span>

14. <span data-ttu-id="7a4ba-149">Si vous avez choisi d’autoriser la collaboration de données dans **Collaboration de données**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-149">If you chose to allow data collaboration in **Data collaboration**, do the following:</span></span>
    
      - <span data-ttu-id="7a4ba-p113">Pour interdire les téléchargements externes, désactivez la case à cocher **Autoriser les participants fédérés et anonymes à télécharger du contenu**. Par défaut, les utilisateurs externes peuvent télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p113">To prevent external downloads, clear the **Allow federated and anonymous participants to download content** check box. By default, external users can download content.</span></span>
    
      - <span data-ttu-id="7a4ba-p114">Pour interdire les transferts de fichiers, désactivez la case à cocher **Autoriser les participants à transférer des fichiers**. Par défaut, les utilisateurs peuvent transférer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p114">To prevent file transfers, clear the **Allow participants to transfer files** check box. By default, users can transfer files.</span></span>
    
      - <span data-ttu-id="7a4ba-154">Pour interdire l’utilisation des annotations, désactivez la case à cocher **Activer les annotations**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-154">To prevent the use of annotations, clear the **Enable annotations** check box.</span></span> <span data-ttu-id="7a4ba-155">Pour utiliser des annotations dans Shard des présentations PowerPoint, désactivez les **Annotations PowerPoint**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-155">To the use of annotations in shard PowerPoint presentations, clear the **Enable PowerPoint annotations**.</span></span> <span data-ttu-id="7a4ba-156">Par défaut, les annotations sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-156">By default, annotations are allowed.</span></span>
    
      - <span data-ttu-id="7a4ba-p116">Pour interdire l’utilisation des sondages, désactivez la case à cocher **Activer les sondages**. Par défaut, les sondages sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p116">To prevent the use of polls, clear the **Enable polls** check box. By default, polls are allowed.</span></span>

15. <span data-ttu-id="7a4ba-159">Dans **Partage d’application**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-159">In **Application sharing**, do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-160">Pour interdire l’utilisation du partage d’application, cliquez sur **Désactiver le partage d’application**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-160">To prevent the use of application sharing, click **Disable application sharing**.</span></span>
    
      - <span data-ttu-id="7a4ba-p117">Pour autoriser l’utilisation du partage d’application, cliquez sur **Activer le partage d’application**. Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p117">To allow the use of application sharing, click **Enable application sharing**. This is the default setting.</span></span>

16. <span data-ttu-id="7a4ba-163">Si vous avez choisi d’autoriser le partage d’application dans **Partage d’application**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-163">If you chose to allow application sharing in **Application sharing**, do the following:</span></span>
    
      - <span data-ttu-id="7a4ba-p118">Pour empêcher les participants à la réunion de prendre le contrôle du partage d’application, désactivez la case à cocher **Autoriser les participants à prendre le contrôle**. Par défaut, les participants peuvent prendre le contrôle du partage d’application.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p118">To prevent meeting participants from taking control of application sharing, clear the **Allow participants to take control** check box. By default, participants can take control of application sharing.</span></span>
    
      - <span data-ttu-id="7a4ba-p119">Si vous avez choisi d’autoriser les participants à la réunion à prendre le contrôle du partage d’application, activez la case à cocher **Autoriser les participants fédérés et anonymes à prendre le contrôle** pour autoriser les utilisateurs externes à prendre le contrôle du partage d’application. Par défaut, les utilisateurs externes ne peuvent pas prendre le contrôle du partage d’application.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p119">If you chose to allow meeting participants to take control of application sharing, select the **Allow federated and anonymous participants to take control** check box to allow external users to take control of application sharing. By default, external users cannot take control of application sharing.</span></span>

17. <span data-ttu-id="7a4ba-168">Sous **Stratégie de participant**, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a4ba-168">Under **Participant policy**, do one of the following:</span></span>
    
      - <span data-ttu-id="7a4ba-169">Pour interdire le partage d’application et le partage du Bureau, cliquez sur **Désactiver le partage d’application et de Bureau**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-169">To prevent both application sharing and desktop sharing, click **Disable application and desktop sharing**.</span></span>
    
      - <span data-ttu-id="7a4ba-170">Pour autoriser le partage d’application mais pas le partage du Bureau, cliquez sur **Activer le partage d’application**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-170">To allow application sharing but not desktop sharing, click **Enable application sharing**.</span></span>
    
      - <span data-ttu-id="7a4ba-p120">Pour autoriser le partage d’application et le partage du Bureau, cliquez sur **Activer le partage d’application et de Bureau**. Il s’agit du paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p120">To allow both application sharing and desktop sharing, click **Enable application and desktop sharing**. This is the default setting.</span></span>

18. <span data-ttu-id="7a4ba-p121">Pour interdire les transferts de fichiers d’homologue à homologue, désactivez la case à cocher **Autoriser le transfert de fichiers entre homologues**. Par défaut, les transferts de fichiers d’homologue à homologue sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p121">To prevent peer-to-peer file transfers, clear the **Enable peer-to-peer file transfer** check box. By default, peer-to-peer file transfers are allowed.</span></span>

19. <span data-ttu-id="7a4ba-p122">Pour autoriser l’enregistrement d’homologue à homologue, activez la case à cocher **Activer l’enregistrement entre homologues**. Par défaut, l’enregistrement d’homologue à homologue n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p122">To allow peer-to-peer recording, select the **Enable peer-to-peer recording** check box. By default, peer-to-peer recording is not allowed.</span></span>

20. <span data-ttu-id="7a4ba-p123">Pour autoriser les participants à participer avec plusieurs flux vidéo, activez la case à cocher **Autoriser les participants à participer avec plusieurs flux vidéo**. Par défaut, les flux vidéo multiples sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-p123">To allow participants to join with multiple video streams, select the **Enable participants to join with multiple video streams** check box. By default, multiple video streams are allowed.</span></span>

21. <span data-ttu-id="7a4ba-179">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-179">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-an-existing-user-or-site-policy"></a><span data-ttu-id="7a4ba-180">Pour modifier une stratégie d’utilisateur ou de site existante</span><span class="sxs-lookup"><span data-stu-id="7a4ba-180">To modify an existing user or site policy</span></span>

1.  <span data-ttu-id="7a4ba-181">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-181">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="7a4ba-182">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-182">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="7a4ba-183">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ba-183">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="7a4ba-184">Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur **stratégie de conférence**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-184">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="7a4ba-185">Dans la liste des stratégies de conférence, cliquez sur la stratégie à modifier, cliquez sur **Modifier**, puis sur **Afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-185">In the list of conferencing policies, click the policy that you want to change, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="7a4ba-186">Dans **Modifier la stratégie de conférence**, modifiez les paramètres de stratégie, à l’exception du nom de la stratégie qui ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-186">In **Edit Conferencing Policy**, modify any of the policy settings, except for the policy name, which cannot be modified.</span></span>

6.  <span data-ttu-id="7a4ba-187">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="7a4ba-187">Click **Commit**.</span></span>

<span data-ttu-id="7a4ba-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a4ba-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

