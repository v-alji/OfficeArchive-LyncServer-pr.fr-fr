---
title: 'Lync Server 2013 : afficher les informations sur les paramètres de configuration de Lync Phone Edition'
description: 'Lync Server 2013 : afficher les informations sur les paramètres de configuration de Lync Phone Edition.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Lync Phone Edition configuration settings information
ms:assetid: 15f94478-651f-4063-9918-6a059f98df16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687976(v=OCS.15)
ms:contentKeyID: 49733564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62719b24920ee72a92b2f80498d5ea2a59288c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440415"
---
# <a name="view-lync-phone-edition-configuration-settings-information-in-lync-server-2013"></a><span data-ttu-id="de722-103">Afficher les informations sur les paramètres de configuration de Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de722-103">View Lync Phone Edition configuration settings information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de722-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de722-104">

<span> </span></span></span>

<span data-ttu-id="de722-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="de722-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="de722-106">Vous pouvez consulter les informations de configuration des appareils exécutant Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="de722-106">You can view configuration information about devices running Lync Phone Edition.</span></span> <span data-ttu-id="de722-107">Les informations sont organisées en collections.</span><span class="sxs-lookup"><span data-stu-id="de722-107">The information is organized into collections.</span></span> <span data-ttu-id="de722-108">Lorsque vous installez Lync Server, vous obtenez un ensemble de paramètres Lync Phone Edition qui s’appliquent à tous les appareils exécutant Lync Phone Edition dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="de722-108">When you install Lync Server, you get a collection of Lync Phone Edition settings that apply to all the devices running Lync Phone Edition in your deployment.</span></span> <span data-ttu-id="de722-109">Vous pouvez également créer de nouvelles collections de paramètres pour un site spécifique.</span><span class="sxs-lookup"><span data-stu-id="de722-109">You can also create new collections of settings for a specific site.</span></span> <span data-ttu-id="de722-110">Les paramètres de site sont prioritaires par rapport aux paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="de722-110">Site settings take precedence over global settings.</span></span> <span data-ttu-id="de722-111">Chaque collection de paramètres est composée d’un nom, de l’étendue (globale ou d’un site), du paramètre de sécurité SIP, du niveau de journalisation, du niveau de qualité de service (QoS), du paramètre de verrouillage du téléphone et des détails du verrouillage du téléphone, c’est-à-dire de la longueur minimale du code confidentiel (PIN) et du temps avant que le téléphone se verrouille.</span><span class="sxs-lookup"><span data-stu-id="de722-111">Each collection of settings consists of a name, the scope (global or site), SIP security setting, logging level, voice quality of service (QoS) level, phone-lock setting, and phone-lock details, that is, the minimum length of the unlock personal identification number (PIN) and time before the phone locks itself.</span></span>

<div>

## <a name="to-view-configuration-information-about-devices-running-lync-phone-edition"></a><span data-ttu-id="de722-112">Pour afficher des informations de configuration sur les appareils exécutant Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="de722-112">To view configuration information about devices running Lync Phone Edition</span></span>

1.  <span data-ttu-id="de722-113">À partir d’un compte d’utilisateur auquel est affecté le rôle CsUserAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="de722-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="de722-114">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="de722-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="de722-115">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="de722-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="de722-116">Dans la barre de navigation de gauche, cliquez sur **clients**, puis sur le bouton navigation de **configuration d’appareil** .</span><span class="sxs-lookup"><span data-stu-id="de722-116">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="de722-117">Dans la page **Configuration des appareils** , cliquez sur l’ensemble de paramètres pour lesquels vous souhaitez afficher les informations.</span><span class="sxs-lookup"><span data-stu-id="de722-117">On the **Device Configuration** page, click the collection of settings you want to view information about.</span></span> <span data-ttu-id="de722-118">Le nom, l’étendue, le paramètre de sécurité SIP, le niveau de qualité de la voix et les paramètres de verrouillage du téléphone apparaissent dans la page principale.</span><span class="sxs-lookup"><span data-stu-id="de722-118">The name, scope, SIP security setting, voice quality level, and phone lock setting are listed on the main page.</span></span> <span data-ttu-id="de722-119">Pour afficher le niveau de journalisation et les détails de verrouillage du téléphone, cliquez sur le menu **modifier** , puis sur **afficher les détails**.</span><span class="sxs-lookup"><span data-stu-id="de722-119">To view the logging level and phone lock details, click the **Edit** menu, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-lync-phone-edition-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="de722-120">Affichage des informations de configuration de Lync Phone Edition à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="de722-120">Viewing Lync Phone Edition Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="de722-121">Vous pouvez afficher les paramètres de configuration de Lync Phone Edition à l’aide de Lync Server Management Shell et de l’applet **de passe Get-CsUCPhoneConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="de722-121">You can view Lync Phone Edition configuration settings by using Lync Server Management Shell and the **Get-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="de722-122">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de722-122">You can run this cmdlet can from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="de722-123">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="de722-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-lync-phone-edition-configuration-information"></a><span data-ttu-id="de722-124">Pour afficher les informations de configuration de Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="de722-124">To view Lync Phone Edition configuration information</span></span>

  - <span data-ttu-id="de722-125">Pour afficher des informations sur les paramètres de configuration de Lync Phone Edition, tapez la commande suivante dans Lync Server Management Shell, puis appuyez sur entrée :</span><span class="sxs-lookup"><span data-stu-id="de722-125">To view information about all your Lync Phone Edition configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsUCPhoneConfiguration
    
    <span data-ttu-id="de722-126">La commande renvoie des informations similaires à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="de722-126">The command returns information similar to the following:</span></span>
    
        Identity             : Global
        CalendarPollInterval : 00:03:00
        EnforcePhoneLock     : True
        PhoneLockTimeout     : 00:10:00
        MinPhonePinLength    : 6
        SIPSecurityMode      : High
        VoiceDiffServTag     : 40
        Voice8021p           : 0
        LoggingLevel         : Off

</div>

<span data-ttu-id="de722-127">Pour plus d’informations, consultez la rubrique [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span><span class="sxs-lookup"><span data-stu-id="de722-127">For details, see [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="de722-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de722-128">See Also</span></span>


[<span data-ttu-id="de722-129">Créer ou modifier un ensemble de paramètres de configuration de Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de722-129">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="de722-130">Supprimer une collection existante de paramètres de configuration de Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de722-130">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="de722-131">Configurer les paramètres de sécurité de Lync Phone Edition dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de722-131">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[<span data-ttu-id="de722-132">Renforcer le verrouillage du téléphone dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de722-132">Enforce phone locking in Lync Server 2013</span></span>](lync-server-2013-enforce-phone-locking.md)  
  

<span data-ttu-id="de722-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de722-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

