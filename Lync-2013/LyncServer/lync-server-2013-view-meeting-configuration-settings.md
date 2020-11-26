---
title: 'Lync Server 2013 : afficher les paramètres de configuration de la réunion'
description: 'Lync Server 2013 : afficher les paramètres de configuration de la réunion.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View meeting configuration settings
ms:assetid: d03a4684-9d8b-4728-917d-5b5c91511e2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721894(v=OCS.15)
ms:contentKeyID: 49733828
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 190b9d331a8cd0a08e17c482dbc3b0bc27590003
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446975"
---
# <a name="view-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="14d9c-103">Afficher les paramètres de configuration de la réunion dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14d9c-103">View meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14d9c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14d9c-104">

<span> </span></span></span>

<span data-ttu-id="14d9c-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="14d9c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="14d9c-106">Dans Lync Server 2013 panneau de configuration, vous utilisez le paramètre de configuration de la réunion pour contrôler l’implémentation des réunions dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="14d9c-106">In Lync Server 2013 Control Panel, you use meeting configuration setting to control how meetings are implemented in your deployment.</span></span> <span data-ttu-id="14d9c-107">Cela inclut les configurations de réunion suivantes :</span><span class="sxs-lookup"><span data-stu-id="14d9c-107">This includes the following meeting configurations:</span></span>

  - <span data-ttu-id="14d9c-108">Configuration globale créée par défaut lors du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="14d9c-108">A global configuration that is created by default when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="14d9c-109">Configurations facultatives de niveau de site et de niveau utilisateur que vous pouvez créer et utiliser pour spécifier le mode d’implémentation des réunions pour des sites ou des utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="14d9c-109">Optional site-level and user-level configurations that you can create and use to specify how meetings are implemented for specific sites or users.</span></span>

<div>

## <a name="to-view-meeting-configuration-settings"></a><span data-ttu-id="14d9c-110">Pour afficher les paramètres de configuration de la réunion</span><span class="sxs-lookup"><span data-stu-id="14d9c-110">To view meeting configuration settings</span></span>

1.  <span data-ttu-id="14d9c-111">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="14d9c-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="14d9c-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="14d9c-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="14d9c-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="14d9c-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="14d9c-114">Dans la barre de navigation de gauche, cliquez sur **Conférence** , puis sur Configuration de la **réunion**.</span><span class="sxs-lookup"><span data-stu-id="14d9c-114">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="14d9c-115">Dans la page **Configuration de la réunion**, cliquez sur la configuration de réunion à afficher.</span><span class="sxs-lookup"><span data-stu-id="14d9c-115">On the **Meeting Configuration** page, click the meeting configuration that you would like to view.</span></span>

5.  <span data-ttu-id="14d9c-116">Dans **modifier le filtre de fichier**, sélectionnez l’option **afficher les détails...**</span><span class="sxs-lookup"><span data-stu-id="14d9c-116">In **Edit File Filter**, select the **Show Details…**</span></span> <span data-ttu-id="14d9c-117">case à cocher.</span><span class="sxs-lookup"><span data-stu-id="14d9c-117">check box.</span></span>
    
    <span data-ttu-id="14d9c-118">**Modifier la configuration de \<policy\> réunion-** s’ouvre et affiche les paramètres de la stratégie sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="14d9c-118">**Edit Meeting Configuration - \<policy\>** opens displaying the settings for the selected policy.</span></span> <span data-ttu-id="14d9c-119">Pour plus d’informations sur la configuration des paramètres, voir [créer ou modifier un ensemble de paramètres de configuration de réunion dans Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="14d9c-119">For details about configuring the settings, see [Create or modify a collection of meeting configuration settings in Lync Server 2013](lync-server-2013-create-or-modify-a-collection-of-meeting-configuration-settings.md).</span></span>

</div>

<div>

## <a name="viewing-meeting-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="14d9c-120">Affichage des informations de configuration de la réunion à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="14d9c-120">Viewing Meeting Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="14d9c-121">Les paramètres de configuration de réunion peuvent être affichés à l’aide de Windows PowerShell et de l’applet de Get-CsMeetingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="14d9c-121">Meeting configuration settings can be viewed by using Windows PowerShell and the Get-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="14d9c-122">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14d9c-122">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="14d9c-123">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="14d9c-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-meeting-configuration-information"></a><span data-ttu-id="14d9c-124">Pour afficher les informations de configuration de la réunion</span><span class="sxs-lookup"><span data-stu-id="14d9c-124">To view meeting configuration information</span></span>

  - <span data-ttu-id="14d9c-125">Pour afficher des informations sur l’ensemble des paramètres de configuration de la réunion, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="14d9c-125">To view information about all your meeting configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsMeetingConfiguration
    
    <span data-ttu-id="14d9c-126">Vous obtiendrez des indications semblables à ceci :</span><span class="sxs-lookup"><span data-stu-id="14d9c-126">That will return information similar to this:</span></span>
    
        Identity                        : Global
        PstnCallersBypassLobby          : True
        EnableAssignedConferenceType    : True
        DesignateAsPresenter            : Company
        AssignedConferenceTypeByDefault : True
        AdmitAnonymousUsersByDefault    : True
        RequireRoomSystemsAuthorization : False
        LogoURL                         :
        LegalURL                        :
        HelpURL                         :
        CustomFooterText                :
        AllowConferenceRecording        : True

</div>

<span data-ttu-id="14d9c-127">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="14d9c-127">For more information, see the help topic for the [Get-CsMeetingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration) cmdlet.</span></span>

<span data-ttu-id="14d9c-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14d9c-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

