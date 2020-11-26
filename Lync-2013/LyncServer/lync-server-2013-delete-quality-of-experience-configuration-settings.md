---
title: 'Lync Server 2013 : supprimer les paramètres de configuration de la qualité de l’apprentissage'
description: 'Lync Server 2013 : supprimer les paramètres de configuration de qualité de l’interface utilisateur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete Quality of Experience configuration settings
ms:assetid: fd0c4c2f-3bfb-42cb-9b6a-f0f8d5aa9e81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182613(v=OCS.15)
ms:contentKeyID: 48185954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1894877fe3dbbc758ba02b0e4e5b81c8b7edc4fb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430426"
---
# <a name="delete-quality-of-experience-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="69f93-103">Supprimer les paramètres de configuration de la qualité de l’interface dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69f93-103">Delete Quality of Experience configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69f93-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69f93-104">

<span> </span></span></span>

<span data-ttu-id="69f93-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="69f93-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="69f93-p101">Les mesures de la qualité de l’expérience (QoE) effectuent le suivi de la qualité des appels audio et vidéo dans votre organisation, y compris le nombre de paquets réseau perdus, le bruit de fond et le montant de « gigue » (différences de retard des paquets). Ces mesures sont stockées dans une base de données distincte des autres données (telles que les enregistrements des détails des appels), ce qui permet d’activer et de désactiver l’enregistrement QoE indépendamment de l’enregistrement des autres données.</span><span class="sxs-lookup"><span data-stu-id="69f93-p101">Quality of Experience (QoE) metrics track the quality of audio and video calls made in your organization, including such things as the number of network packets lost, background noise, and the amount of "jitter" (differences in packet delay). These metrics are stored in a database apart from other data (such as call detail records), which allows you to enable and disable QoE independent of other data recording.</span></span>

<span data-ttu-id="69f93-108">Lorsque vous installez Microsoft Lync Server 2013, une collection globale unique de paramètres de configuration QoE est créée pour vous.</span><span class="sxs-lookup"><span data-stu-id="69f93-108">When you install Microsoft Lync Server 2013, a single, global collection of QoE configuration settings is created for you.</span></span> <span data-ttu-id="69f93-109">Les administrateurs peuvent également créer des collections de paramètres personnalisés pouvant être appliquées aux sites individuels.</span><span class="sxs-lookup"><span data-stu-id="69f93-109">Administrators also have the option of creating custom setting collections that can be applied to individual sites.</span></span> <span data-ttu-id="69f93-110">Par conception, les paramètres configurés sur l’étendue Site sont prioritaires sur les paramètres configurés sur l’étendue Global.</span><span class="sxs-lookup"><span data-stu-id="69f93-110">By design, settings configured at the site scope take precedence over settings configured at the global scope.</span></span> <span data-ttu-id="69f93-111">Si vous supprimez les paramètres sur l’étendue Site, la QoE sera gérée dans ce site en utilisant les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="69f93-111">If you delete site-scoped settings, then QoE will be managed in that site by using the global settings.</span></span>

<span data-ttu-id="69f93-p103">Notez que vous pouvez également « supprimer » les paramètres globaux. Cependant, les paramètres globaux ne seront pas réellement supprimés. Toutes les propriétés de la collection seront en revanche réinitialisées à leurs valeurs par défaut. Par exemple, la purge est activée par défaut dans une collection de paramètres de configuration QoE. Supposons que vous modifiez la collection globale pour que la purge soit désactivée. Si vous supprimez ultérieurement les paramètres globaux, toutes les propriétés seront réinitialisées à leurs valeurs par défaut. Dans ce cas, cela signifie que la purge sera de nouveau activée.</span><span class="sxs-lookup"><span data-stu-id="69f93-p103">Note that you can also “delete” the global settings. However, the global settings will not actually be removed. Instead, all the properties in that collection will be reset to their default values. For example, by default purging is enabled in a collection of QoE configuration settings. Suppose you modify the global collection so that purging is disabled. If you later delete the global settings, all the properties will be reset to their default values. In this case, that means that purging will once again be enabled.</span></span>

<span data-ttu-id="69f93-119">Vous pouvez supprimer les paramètres de configuration QoE en utilisant le panneau de configuration de Lync Server ou en utilisant l’applet de commande [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="69f93-119">You can remove QoE configuration settings by using the Lync Server Control Panel or by using the [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration) cmdlet.</span></span>

<div>

## <a name="to-delete-qoe-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="69f93-120">Pour supprimer les paramètres de configuration QoE en utilisant le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="69f93-120">To delete QoE configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="69f93-121">Connectez-vous à l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="69f93-121">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="69f93-122">Pour plus d’informations, reportez-vous à la section [délégation des autorisations de configuration dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="69f93-122">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="69f93-123">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="69f93-123">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="69f93-124">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="69f93-124">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="69f93-125">Dans la barre de navigation de gauche, cliquez sur **Surveillance et archivage**, puis cliquez sur **Données de qualité de l’expérience**.</span><span class="sxs-lookup"><span data-stu-id="69f93-125">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="69f93-126">Sur la page **Données QoE**, cliquez sur la stratégie de votre choix, puis sur **Modifier**, et enfin sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="69f93-126">On the **Quality of Experience Data** page, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="69f93-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="69f93-127">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-qoe-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="69f93-128">Suppression des paramètres de configuration QoE à l’aide d’applets de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="69f93-128">Removing QoE Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="69f93-129">Vous pouvez supprimer des paramètres de configuration QoE à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsQoEConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="69f93-129">You can delete QoE configuration settings by using Windows PowerShell and the **Remove-CsQoEConfiguration** cmdlet.</span></span> <span data-ttu-id="69f93-130">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69f93-130">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="69f93-131">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="69f93-131">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-qoe-configuration-settings"></a><span data-ttu-id="69f93-132">Pour supprimer une collection spécifiée de paramètres de configuration QoE</span><span class="sxs-lookup"><span data-stu-id="69f93-132">To remove a specified collection of QoE configuration settings</span></span>

  - <span data-ttu-id="69f93-133">Cette commande supprime les paramètres de configuration QoE appliqués au site Redmond :</span><span class="sxs-lookup"><span data-stu-id="69f93-133">This command removes the QoE configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsQoEConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-qoe-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="69f93-134">Pour supprimer tous les paramètres de configuration QoE appliqués à l’étendue Site</span><span class="sxs-lookup"><span data-stu-id="69f93-134">To remove all of the QoE configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="69f93-135">Cette commande supprime tous les paramètres de configuration QoE appliqués à l’étendue Site :</span><span class="sxs-lookup"><span data-stu-id="69f93-135">This command removes all the QoE configuration settings applied to the site scope:</span></span>
    
        Get-CsQoEConfiguration -Filter "site:*" | Remove-CsQoEConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-qoe-configuration-settings-where-qoe-monitoring-is-disabled"></a><span data-ttu-id="69f93-136">Pour supprimer tous les paramètres de configuration QoE lorsque le suivi QoE est désactivé</span><span class="sxs-lookup"><span data-stu-id="69f93-136">To remove all of the QoE configuration settings where QoE monitoring is disabled</span></span>

  - <span data-ttu-id="69f93-137">Cette commande supprime tous les paramètres de configuration QoE lorsque le suivi QoE est désactivé :</span><span class="sxs-lookup"><span data-stu-id="69f93-137">This command removes all the QoE configuration settings where QoE monitoring has been disabled:</span></span>
    
        Get-CsQoEConfiguration | Where-Object {$_.EnableQoE -eq $False} | Remove-CsQoEConfiguration

</div>

<span data-ttu-id="69f93-138">Pour plus d’informations, consultez la rubrique [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration).</span><span class="sxs-lookup"><span data-stu-id="69f93-138">For details, see [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration).</span></span>

<span data-ttu-id="69f93-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69f93-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

