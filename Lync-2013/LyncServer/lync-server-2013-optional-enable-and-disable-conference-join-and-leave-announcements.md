---
title: (Facultatif) Activation et désactivation des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence
description: Facultatif Activez et désactivez l’Association de conférences et quittez les annonces.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Enable and disable conference join and leave announcements
ms:assetid: c9529568-e66c-48d8-aef2-9072f9c336ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398834(v=OCS.15)
ms:contentKeyID: 48185403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70cd6b452a44d7d40f23d5ca96b6e4b7b063d2ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445238"
---
# <a name="optional-enable-and-disable-conference-join-and-leave-announcements-in-lync-server-2013"></a><span data-ttu-id="c4c9d-103">(Facultatif) Activation et désactivation des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4c9d-103">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4c9d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4c9d-104">

<span> </span></span></span>

<span data-ttu-id="c4c9d-105">_**Dernière modification de la rubrique :** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="c4c9d-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="c4c9d-106">Lorsque des utilisateurs d’appels entrants rejoignent ou quittent une conférence, l’application d’annonce d’annonce peut annoncer leur ouverture ou leur sortie en jouant un message ou en prononçant leurs noms.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-106">When dial-in users join or leave a conference, the Conferencing Announcement application can announce their entrance or exit by playing a tone or saying their names.</span></span> <span data-ttu-id="c4c9d-107">Vous pouvez modifier le fonctionnement des annonces en exécutant des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-107">You can change how announcements work by running cmdlets.</span></span> <span data-ttu-id="c4c9d-108">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-108">This step is optional.</span></span>

<div>

## <a name="to-modify-the-conference-join-and-leave-announcement-behavior"></a><span data-ttu-id="c4c9d-109">Pour modifier le comportement des annonces indiquant qu’un utilisateur rejoint ou quitte une conférence</span><span class="sxs-lookup"><span data-stu-id="c4c9d-109">To modify the conference join and leave announcement behavior</span></span>

1.  <span data-ttu-id="c4c9d-110">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle **CS-ServerAdministrator** ou **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="c4c9d-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="c4c9d-111">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c4c9d-112">Exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="c4c9d-112">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingConfiguration
    
    <span data-ttu-id="c4c9d-113">Cette applet de connexion récupère des informations sur la nécessité pour les participants d’enregistrer leur nom lorsqu’ils rejoignent une conférence et de la manière dont Lync Server répond lorsque les participants rejoignent ou quittent une conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-113">This cmdlet retrieves information about whether participants are required to record their name when joining a conference and how Lync Server responds when participants join or leave a dial-in conference.</span></span>

4.  <span data-ttu-id="c4c9d-114">Exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="c4c9d-114">Run the following at the command prompt:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity <identity of dial-in conferencing settings to be modified>
        [-EnableNameRecording <$true | $false>]
        [-EntryExitAnnouncementsEnabledByDefault <$true | $false>]
        [-EntryExitAnnouncementsType <UseNames | ToneOnly]
    
    <span data-ttu-id="c4c9d-115">**EnableNameRecording**   Détermine si les participants anonymes sont invités à enregistrer leur nom avant de participer à la Conférence.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-115">**EnableNameRecording**   Determines whether anonymous participants are asked to record their name before entering the conference.</span></span> <span data-ttu-id="c4c9d-116">La valeur par défaut est « $true », ce qui signifie que les participants anonymes sont invités à donner leur nom avant de participer à une conférence.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-116">The default value is "$true," which means that anonymous participants are prompted to state their name when joining a conference.</span></span> <span data-ttu-id="c4c9d-117">(Les participants authentifiés ne sont pas tenus d’indiquer leur nom, car leur nom complet est utilisé.)</span><span class="sxs-lookup"><span data-stu-id="c4c9d-117">(Authenticated participants do not record their name because their display name is used instead.)</span></span>
    
    <span data-ttu-id="c4c9d-118">**EntryExitAnnouncementsEnabledByDefault**   Indique si l’annonce est activée ou désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-118">**EntryExitAnnouncementsEnabledByDefault**   Indicates whether announcements are turned on or off by default.</span></span> <span data-ttu-id="c4c9d-119">La valeur par défaut est « $false », ce qui signifie qu’aucune annonce n’est effectuée lorsque les participants rejoignent ou quittent une conférence.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-119">The default value is "$false," which means that by default there are no announcements when participants join or leave a conference.</span></span> <span data-ttu-id="c4c9d-120">Lorsqu’il planifie une réunion, l’organisateur peut ignorer ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-120">The meeting organizer can override this setting when scheduling a meeting.</span></span>
    
    <span data-ttu-id="c4c9d-121">**EntryExitAnnouncementsType**   Indique l’action effectuée dès qu’un participant rejoint ou quitte une conférence pour laquelle les annonces sont activées.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-121">**EntryExitAnnouncementsType**   Indicates the action taken whenever a participant joins or leaves a conference for which announcements are enabled.</span></span> <span data-ttu-id="c4c9d-122">La valeur par défaut est « UseNames », ce qui signifie qu’une annonce similaire à la suivante est effectuée : « Ken Myer a rejoint la conférence » lorsque les annonces sont activées.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-122">The default value is "UseNames," which means there is an announcement similar to the following: "Ken Myer has joined the conference" when announcements are turned on.</span></span>
    
    <span data-ttu-id="c4c9d-p105">Vous pouvez configurer ces paramètres globalement ou au niveau d’un site. (Les paramètres configurés au niveau du site sont prioritaires sur les paramètres configurés au niveau global.)</span><span class="sxs-lookup"><span data-stu-id="c4c9d-p105">You can configure these settings at the global scope or at the site scope. Settings configured at the site scope take precedence over settings configured at the global scope.</span></span>
    
    <span data-ttu-id="c4c9d-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c4c9d-125">For example:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity site:Redmond
        -EnableNameRecording $false
        -EntryExitAnnouncementsEnabledByDefault $true
        -EntryExitAnnouncementsType ToneOnly
    
    <span data-ttu-id="c4c9d-126">Dans cet exemple, les paramètres sont configurés dans l’étendue du site de Redmond.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-126">In this example, settings are configured at the site scope for Redmond.</span></span> <span data-ttu-id="c4c9d-127">Les annonces sont activées, mais les participants ne sont pas invités à donner leur nom lorsqu’ils rejoignent une conférence.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-127">Announcements are turned on, but participants are not prompted to say their name when they join a conference.</span></span> <span data-ttu-id="c4c9d-128">Une tonalité est lue lorsque les participants entrent ou quittent une conférence.</span><span class="sxs-lookup"><span data-stu-id="c4c9d-128">A tone is played when participants enter or leave a conference.</span></span>

<span data-ttu-id="c4c9d-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4c9d-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

