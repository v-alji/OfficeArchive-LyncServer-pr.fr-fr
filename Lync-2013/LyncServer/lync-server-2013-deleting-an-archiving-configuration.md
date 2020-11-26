---
title: 'Lync Server 2013 : suppression d’une configuration de l’archivage'
description: 'Lync Server 2013 : suppression d’une configuration d’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting an Archiving configuration
ms:assetid: a8744d39-5cf2-474c-9a99-a0f3a37f846f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205167(v=OCS.15)
ms:contentKeyID: 48185093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9bb267c119b49c9bbf06f365c3bdf2cbab459628
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430377"
---
# <a name="deleting-an-archiving-configuration-in-lync-server-2013"></a><span data-ttu-id="ee527-103">Suppression d’une configuration d’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee527-103">Deleting an Archiving configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee527-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee527-104">

<span> </span></span></span>

<span data-ttu-id="ee527-105">_**Dernière modification de la rubrique :** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ee527-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ee527-106">Vous pouvez supprimer une configuration de pool ou de configuration de site.</span><span class="sxs-lookup"><span data-stu-id="ee527-106">You can delete a site configuration or pool configuration.</span></span> <span data-ttu-id="ee527-107">La configuration globale ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="ee527-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="ee527-108">Si vous supprimez la configuration globale, ses valeurs par défaut sont automatiquement rétablies.</span><span class="sxs-lookup"><span data-stu-id="ee527-108">If you delete the global configuration, it is automatically reset to the default values.</span></span> <span data-ttu-id="ee527-109">Pour plus d’informations sur l’implémentation des configurations d’archivage, notamment les options que vous pouvez spécifier et la hiérarchie des configurations d’archivage, voir fonctionnement [de l’archivage dans Lync Server 2013](lync-server-2013-how-archiving-works.md) dans la documentation de planification, la documentation de déploiement ou les opérations.</span><span class="sxs-lookup"><span data-stu-id="ee527-109">For details about how Archiving configurations are implemented, including which options you can specify and the hierarchy of Archiving configurations, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>

## <a name="to-delete-a-site-or-pool-configuration-for-archiving"></a><span data-ttu-id="ee527-110">Pour supprimer une configuration de site ou de pool pour l’archivage</span><span class="sxs-lookup"><span data-stu-id="ee527-110">To delete a site or pool configuration for archiving</span></span>

1.  <span data-ttu-id="ee527-111">À partir d’un compte d’utilisateur auquel est affecté un des rôles CsArchivingAdministrator ou CsAdministrator, ouvrez une session sur un ordinateur de votre déploiement interne.</span><span class="sxs-lookup"><span data-stu-id="ee527-111">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ee527-112">Ouvrez une fenêtre de navigateur, puis entrez l’URL d’administration pour ouvrir le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee527-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ee527-113">Pour plus d’informations sur les différentes méthodes que vous pouvez utiliser pour démarrer le panneau de configuration de Lync Server, voir [ouvrir les outils d’administration de Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ee527-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ee527-114">Dans la barre de navigation gauche, cliquez sur **surveillance et archivage**, puis cliquez sur **configuration de l’archivage**.</span><span class="sxs-lookup"><span data-stu-id="ee527-114">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Configuration**.</span></span>

4.  <span data-ttu-id="ee527-115">Dans la liste des configurations d’archivage, cliquez sur la configuration de site ou de pool que vous souhaitez supprimer, cliquez sur **Modifier**, puis cliquez sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="ee527-115">In the list of archiving configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="ee527-116">Cliquez sur **Valider**.</span><span class="sxs-lookup"><span data-stu-id="ee527-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="removing-archiving-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ee527-117">Supprimer les paramètres de configuration de l’archivage à l’aide des cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee527-117">Removing Archiving Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ee527-118">Vous pouvez supprimer des paramètres de configuration de l’archivage à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsArchivingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ee527-118">Archiving configuration settings can be deleted by using Windows PowerShell and the **Remove-CsArchivingConfiguration** cmdlet.</span></span> <span data-ttu-id="ee527-119">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee527-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ee527-120">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ee527-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-archiving-configuration-settings"></a><span data-ttu-id="ee527-121">Pour supprimer une collection spécifiée de paramètres de configuration de l’archivage</span><span class="sxs-lookup"><span data-stu-id="ee527-121">To remove a specified collection of archiving configuration settings</span></span>

  - <span data-ttu-id="ee527-122">La commande suivante supprime les paramètres de configuration de l’archivage appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="ee527-122">The following command removes the archiving configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsArchivingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-archiving-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="ee527-123">Pour supprimer tous les paramètres de configuration de l’archivage appliqués à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="ee527-123">To remove all the archiving configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="ee527-124">Cette commande supprime tous les paramètres de configuration de l’archivage appliqués à l’étendue du service :</span><span class="sxs-lookup"><span data-stu-id="ee527-124">This command removes all the archiving configuration settings applied to the service scope:</span></span>
    
        Get-CsArchivingConfiguration -Filter "site:*" | Remove-CsArchivingConfiguration

</div>

<div>

## <a name="to-remove-archiving-configuration-settings-based-on-a-specified-property-value"></a><span data-ttu-id="ee527-125">Pour supprimer les paramètres de configuration de l’archivage en fonction d’une valeur de propriété spécifiée</span><span class="sxs-lookup"><span data-stu-id="ee527-125">To remove archiving configuration settings based on a specified property value</span></span>

  - <span data-ttu-id="ee527-126">Cette commande supprime tous les paramètres de configuration de l’archivage dans lesquels l’archivage Exchange a été désactivé :</span><span class="sxs-lookup"><span data-stu-id="ee527-126">This command removes all the archiving configuration settings where Exchange archiving has been disabled:</span></span>
    
        Get-CsArchivingConfiguration | Where-Object {$_.EnableExchangeArchiving -eq $False} | Remove-CsArchivingConfiguration

</div>

<span data-ttu-id="ee527-127">Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="ee527-127">For more information, see the help topic for the [Remove-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsArchivingConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee527-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee527-128">See Also</span></span>


[<span data-ttu-id="ee527-129">Fonctionnement de l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee527-129">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)  


[<span data-ttu-id="ee527-130">Gestion de l’archivage des communications internes et externes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee527-130">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

<span data-ttu-id="ee527-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee527-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

