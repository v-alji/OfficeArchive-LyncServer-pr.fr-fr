---
title: 'Lync Server 2013 : afficher les informations de stratégie de conférence'
description: 'Lync Server 2013 : afficher les informations de stratégie de conférence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View conferencing policy information
ms:assetid: e99fdc4d-926a-4e36-ac99-ab5035568847
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721918(v=OCS.15)
ms:contentKeyID: 49733852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e463c500e48f4032c8dab3a3787715f7265be9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438651"
---
# <a name="view-conferencing-policy-information-in-lync-server-2013"></a><span data-ttu-id="8617b-103">Afficher les informations de stratégie de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8617b-103">View conferencing policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8617b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8617b-104">

<span> </span></span></span>

<span data-ttu-id="8617b-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8617b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8617b-106">Dans Lync Server 2013 panneau de configuration, vous utilisez des stratégies de conférence pour contrôler la façon dont les conférences sont implémentées dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="8617b-106">In Lync Server 2013 Control Panel, you use conferencing policies to control how conferencing is implemented in your deployment.</span></span> <span data-ttu-id="8617b-107">Cela inclut les stratégies de conférence suivantes :</span><span class="sxs-lookup"><span data-stu-id="8617b-107">This includes the following conferencing policies:</span></span>

  - <span data-ttu-id="8617b-108">Stratégie globale créée par défaut lors du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8617b-108">A global policy that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="8617b-109">Stratégie de niveau de site et de niveau utilisateur facultative que vous pouvez créer et utiliser pour spécifier la façon dont les conférences sont implémentées pour des sites ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8617b-109">Optional site-level and user-level policy that you can create and use to specify how conferencing is implemented for specific sites or users.</span></span>

<div>

## <a name="to-view-conferencing-policy-settings"></a><span data-ttu-id="8617b-110">Pour afficher les paramètres de stratégie de conférence</span><span class="sxs-lookup"><span data-stu-id="8617b-110">To view conferencing policy settings</span></span>

1.  <span data-ttu-id="8617b-111">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="8617b-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8617b-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8617b-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8617b-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8617b-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8617b-114">Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur **stratégie de conférence**.</span><span class="sxs-lookup"><span data-stu-id="8617b-114">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="8617b-115">Dans la page **Stratégie de conférence**, double-cliquez sur la stratégie de conférence à afficher.</span><span class="sxs-lookup"><span data-stu-id="8617b-115">On the **Conferencing Policy** page, double-click the conferencing policy that you would like to view.</span></span>

5.  <span data-ttu-id="8617b-116">Dans **modifier le filtre de fichier**, sélectionnez l’option **afficher les détails...**</span><span class="sxs-lookup"><span data-stu-id="8617b-116">In **Edit File Filter**, select the **Show Details…**</span></span> <span data-ttu-id="8617b-117">case à cocher.</span><span class="sxs-lookup"><span data-stu-id="8617b-117">check box.</span></span>
    
    <span data-ttu-id="8617b-118">**Modifier une stratégie de \<policy\> Conférence-** s’ouvre et affiche les paramètres de la stratégie sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8617b-118">**Edit Conferencing Policy - \<policy\>** opens displaying the settings for the selected policy.</span></span> <span data-ttu-id="8617b-119">Pour plus d’informations sur la configuration des paramètres, consultez la rubrique [créer ou modifier une stratégie de conférence dans Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8617b-119">For details about configuring the settings, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md).</span></span>

</div>

<div>

## <a name="viewing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8617b-120">Affichage de stratégies de conférence à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8617b-120">Viewing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8617b-121">Vous pouvez afficher les stratégies de conférence à l’aide de Windows PowerShell et de l’applet de Get-CsConferencingPolicy.</span><span class="sxs-lookup"><span data-stu-id="8617b-121">Conferencing policies can be viewed by using Windows PowerShell and the Get-CsConferencingPolicy cmdlet.</span></span> <span data-ttu-id="8617b-122">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8617b-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="8617b-123">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="8617b-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-conferencing-policies"></a><span data-ttu-id="8617b-124">Pour afficher les stratégies de conférence</span><span class="sxs-lookup"><span data-stu-id="8617b-124">To view conferencing policies</span></span>

  - <span data-ttu-id="8617b-125">Pour afficher des informations sur toutes vos stratégies de conférence, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="8617b-125">To view information about all your conferencing policies, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsConferencingPolicy
    
    <span data-ttu-id="8617b-126">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="8617b-126">That will return information similar to this:</span></span>
    
        Identity                                  : Global
        AllowIPAudio                              : True
        AllowIPVideo                              : True
        AllowMultiView                            : True
        Description                               :
        AllowParticipantControl                   : True
        AllowAnnotations                          : True
        DisablePowerPointAnnotations              : False
        AllowUserToScheduleMeetingsWithAppSharing : True
        AllowNonEnterpriseVoiceUsersToDialOut     : False
        AllowAnonymousUsersToDialOut              : False
        AllowAnonymousParticipantsInMeetings      : True
        AllowExternalUsersToSaveContent           : True
        AllowExternalUserControl                  : False
        AllowExternalUsersToRecordMeeting         : False
        AllowPolls                                : True
        AllowSharedNotes                          : True
        EnableDialInConferencing                  : True
        EnableAppDesktopSharing                   : Desktop
        AllowConferenceRecording                  : False
        EnableP2PRecording                        : False
        EnableFileTransfer                        : True
        EnableP2PFileTransfer                     : True
        EnableP2PVideo                            : True
        AllowLargeMeetings                        : False
        EnableDataCollaboration                   : True
        MaxVideoConferenceResolution              : VGA
        MaxMeetingSize                            : 250
        AudioBitRateKb                            : 200
        VideoBitRateKb                            : 50000
        AppSharingBitRateKb                       : 50000
        FileTransferBitRateKb                     : 50000
        TotalReceiveVideoBitRateKb                : 6000
        EnableMultiViewJoin                       : True

</div>

<span data-ttu-id="8617b-127">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsConferencingPolicy) .</span><span class="sxs-lookup"><span data-stu-id="8617b-127">For more information, see the help topic for the [Get-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsConferencingPolicy) cmdlet.</span></span>

<span data-ttu-id="8617b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8617b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

