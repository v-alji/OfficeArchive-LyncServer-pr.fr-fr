---
title: Suppression d’une collection de paramètres de configuration de jonction SIP (Session Initiation Protocol) existante
description: Supprimez une collection existante de paramètres de configuration de Trunk SIP.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of SIP trunk configuration settings
ms:assetid: 3b25f14d-884b-42dd-a866-460d276d3e43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688024(v=OCS.15)
ms:contentKeyID: 49733614
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98acede458d34eb30202d898414b2e17076d32d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430517"
---
# <a name="delete-an-existing-collection-of-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="7b8f1-103">Supprimer une collection existante de paramètres de configuration de Trunk SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b8f1-103">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b8f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b8f1-104">

<span> </span></span></span>

<span data-ttu-id="7b8f1-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="7b8f1-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="7b8f1-106">Les paramètres de configuration du Trunk SIP définissent la relation et les fonctionnalités entre un serveur de médiation et la passerelle de réseau téléphonique commuté (PSTN), un échange de succursale public (PBX) ou un contrôleur de bordure de session (SBC) au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="7b8f1-107">Ces paramètres spécifient, par exemple :</span><span class="sxs-lookup"><span data-stu-id="7b8f1-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="7b8f1-108">si la déviation du trafic multimédia doit être activée sur les jonctions ;</span><span class="sxs-lookup"><span data-stu-id="7b8f1-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="7b8f1-109">Les conditions dans lesquelles les paquets de contrôle de transport en temps réel (RTCP) sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="7b8f1-110">Le chiffrement SRTP (Secure Real-Time Protocol) est requis sur chaque Trunk.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="7b8f1-111">Lorsque vous installez Microsoft Lync Server 2013, une collection globale de paramètres de configuration de Trunk SIP est créée pour vous.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="7b8f1-112">Cette collection globale de paramètres ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-112">This global collection of settings cannot be deleted.</span></span> <span data-ttu-id="7b8f1-113">Toutefois, vous pouvez utiliser le panneau de configuration de Lync Server ou l’applet de commande [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) pour « réinitialiser » les propriétés de la collection globale à leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-113">However, you can use the Lync Server Control Panel or the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet to "reset" the properties in the global collection to their default values.</span></span> <span data-ttu-id="7b8f1-114">Par exemple, si vous avez défini la propriété Enable3pccRefer sur true, lorsque vous réinitialisez la collection globale, la propriété Enable3pccRefer rétablira sa valeur par défaut false.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-114">For example, if you have set the Enable3pccRefer property to True, when you reset the global collection the Enable3pccRefer property will revert to its default value of False.</span></span>

<span data-ttu-id="7b8f1-p103">Les administrateurs peuvent aussi créer des paramètres de configuration de jonction personnalisés étendus à un site ou un service (pour une passerelle RTC individuelle). Ces paramètres personnalisés peuvent être supprimés. Lors de la suppression de ces paramètres personnalisés, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="7b8f1-p103">Administrators can also create custom trunk configuration settings at the site scope or at the service scope (for an individual PSTN gateway); these custom settings can be removed. When removing these custom settings keep the following in mind:</span></span>

  - <span data-ttu-id="7b8f1-p104">Si vous supprimez des paramètres étendus à un service, la jonction SIP (Session Initiation Protocol) gérée par ces paramètres est gérée par les paramètres appliqués à son site, le cas échéant. En l’absence de paramètres de site, la jonction est gérée par la collection globale de paramètres de configuration de jonction.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-p104">If you remove service scope settings, then the SIP trunk managed by those settings will be managed by the settings applied to their site, if they exist. If site settings do not exist, those trunks will then be managed by the global collection of trunk configuration settings.</span></span>

  - <span data-ttu-id="7b8f1-119">Si vous supprimez des paramètres étendus à un site, les jonctions SIP (Session Initiation Protocol) gérées par ces paramètres sont alors gérées par la collection globale de paramètres de configuration de jonction.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-119">If you remove site-scoped settings then any SIP trunks managed by those settings will now be managed by the global collection of trunk configuration settings.</span></span>

<div>

## <a name="to-remove-trunk-configuration-settings-with-lync-server-control-panel"></a><span data-ttu-id="7b8f1-120">Pour supprimer les paramètres de configuration de Trunk avec le panneau de configuration de Lync Server</span><span class="sxs-lookup"><span data-stu-id="7b8f1-120">To remove trunk configuration settings with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="7b8f1-121">Dans le panneau de configuration de Lync Server, cliquez sur **routage des communications vocales** , puis cliquez sur **configuration de Trunk**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-121">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="7b8f1-p105">Sous l’onglet **Configuration de la jonction**, sélectionnez la collection de paramètres de configuration de jonction SIP (Session Initiation Protocol) à supprimer, cliquez sur **Modifier**, puis sur **Supprimer**. Pour supprimer plusieurs collections en une seule opération, cliquez sur la première collection à supprimer, maintenez la touche Ctrl enfoncée et cliquez sur les autres collections à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-p105">On the **Trunk Configuration** tab, select the collection of SIP trunk configuration settings to be deleted, click **Edit** and then click **Delete**. To delete multiple collections in the same operation, click the first collection to be deleted, then hold down the Ctrl key and click any additional collections that you want to remove.</span></span>

3.  <span data-ttu-id="7b8f1-p106">La propriété **État** de la collection est définie sur la valeur **Non validé**. Pour valider les modifications et supprimer la collection, cliquez sur **Valider**, puis sur **Tout valider**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-p106">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

4.  <span data-ttu-id="7b8f1-126">Dans la boîte de dialogue **Paramètres de configuration de la voix non validés**, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-126">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

5.  <span data-ttu-id="7b8f1-127">Dans la boîte de dialogue **panneau de configuration Microsoft Lync Server 2013** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-127">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

6.  <span data-ttu-id="7b8f1-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span></span> <span data-ttu-id="7b8f1-129">Lorsque la boîte de dialogue **panneau de configuration Microsoft Lync Server 2013** s’affiche, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-129">When the **Microsoft Lync Server 2013 Control Panel** dialog box appears, click **OK**.</span></span>

</div>

<div>

## <a name="removing-trunk-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="7b8f1-130">Supprimer les paramètres de configuration de ligne à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7b8f1-130">Removing Trunk Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="7b8f1-131">Vous pouvez supprimer des paramètres de configuration d’une ligne à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsTrunkConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7b8f1-131">You can delete trunk configuration settings by using Windows PowerShell and the **Remove-CsTrunkConfiguration** cmdlet.</span></span> <span data-ttu-id="7b8f1-132">Vous pouvez exécuter cette applet de commande sur Lync Server 2013 Management Shell ou à partir d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7b8f1-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="7b8f1-133">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="7b8f1-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-settings"></a><span data-ttu-id="7b8f1-134">Pour supprimer une collection de paramètres spécifiée</span><span class="sxs-lookup"><span data-stu-id="7b8f1-134">To remove a specified collection of settings</span></span>

  - <span data-ttu-id="7b8f1-135">La commande ci-dessous supprime les paramètres de configuration de jonction appliqués au site Redmond :</span><span class="sxs-lookup"><span data-stu-id="7b8f1-135">The following command removes the trunk configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsTrunkConfiguration -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-collections-applied-to-the-site-scope"></a><span data-ttu-id="7b8f1-136">Pour supprimer toutes les collections appliquées dans l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="7b8f1-136">To remove all the collections applied to the site scope</span></span>

  - <span data-ttu-id="7b8f1-137">Cette commande supprime tous les paramètres de configuration de jonction appliqués dans l’étendue du site :</span><span class="sxs-lookup"><span data-stu-id="7b8f1-137">This command removes all the trunk configuration settings applied to the service scope:</span></span>
    
        Get-CsTrunkConfiguration -Filter "service:*" | Remove-CsTrunkConfiguration

</div>

<div>

## <a name="to-remove-all-the-collections-where-media-bypass-is-enabled"></a><span data-ttu-id="7b8f1-138">Pour supprimer toutes les collections pour lesquelles la déviation du trafic multimédia est activée</span><span class="sxs-lookup"><span data-stu-id="7b8f1-138">To remove all the collections where media bypass is enabled</span></span>

  - <span data-ttu-id="7b8f1-139">La commande ci-dessous supprime tous les paramètres de configuration de jonction pour lesquels la déviation du trafic multimédia est activée :</span><span class="sxs-lookup"><span data-stu-id="7b8f1-139">The following command removes all the trunk configuration settings where media bypass has been enabled:</span></span>
    
        Get-CsTrunkConfiguration | Where-Object {$_.EnableBypass -eq $True} | Remove-CsTrunkConfiguration

</div>

<span data-ttu-id="7b8f1-140">Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="7b8f1-140">For more information, see the help topic for the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="7b8f1-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b8f1-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

