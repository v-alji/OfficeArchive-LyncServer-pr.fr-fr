---
title: 'Lync Server 2013 : supprimer une collection de paramètres de configuration de la mise à jour de l’appareil'
description: 'Lync Server 2013 : supprimer une collection de paramètres de configuration de la mise à jour de l’appareil.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a collection of Device Update configuration settings
ms:assetid: 1a649136-34a9-42a7-a5b3-a78bbfe93f36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994019(v=OCS.15)
ms:contentKeyID: 51803928
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3a03227869f68a52a30ea94db33bfb954b7e122
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430713"
---
# <a name="delete-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="037ce-103">Supprimer un ensemble de paramètres de configuration de la mise à jour de périphériques dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="037ce-103">Delete a collection of Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="037ce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="037ce-104">

<span> </span></span></span>

<span data-ttu-id="037ce-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="037ce-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="037ce-106">Les paramètres de configuration de la mise à jour de l’appareil peuvent également être supprimés à l’aide de Windows PowerShell et de l’applet de passe **Remove-CsdeviceUpdateConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="037ce-106">Device update configuration settings can also be deleted by using Windows PowerShell and the **Remove-CsdeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="037ce-107">Cette applet de commande peut être exécutée à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="037ce-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="037ce-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="037ce-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="to-remove-a-specific-collection-of-device-update-configuration-settings"></a><span data-ttu-id="037ce-109">Pour supprimer une collection spécifique de paramètres de configuration de la mise à jour de l’appareil</span><span class="sxs-lookup"><span data-stu-id="037ce-109">To remove a specific collection of device update configuration settings</span></span>

  - <span data-ttu-id="037ce-110">Cette commande supprime les paramètres de configuration de la mise à jour de l’appareil appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="037ce-110">This command deletes the device update configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsDeviceUpdateConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-device-update-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="037ce-111">Pour supprimer tous les paramètres de configuration de la mise à jour de l’appareil appliqués à l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="037ce-111">To remove all the device update configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="037ce-112">Cette commande supprime tous les paramètres de configuration de la mise à jour de l’appareil appliqués à l’étendue du site :</span><span class="sxs-lookup"><span data-stu-id="037ce-112">This command deletes all the device update configuration settings applied to the site scope:</span></span>
    
        Get-CsDeviceUpdateConfiguration -Filter "site:*" | Remove-CsDeviceUpdateConfiguration

</div>

<div>

## <a name="to-remove-device-update-configuration-settings-based-on-the-value-of-the-logcleanupinterval-property"></a><span data-ttu-id="037ce-113">Pour supprimer les paramètres de configuration de la mise à jour de périphériques en fonction de la valeur de la propriété LogCleanUpInterval</span><span class="sxs-lookup"><span data-stu-id="037ce-113">To remove device update configuration settings based on the value of the LogCleanUpInterval property</span></span>

  - <span data-ttu-id="037ce-114">La commande suivante supprime tous les paramètres de configuration de la mise à jour de l’appareil, où l’intervalle de nettoyage du journal est supérieur à 10 jours (10,00:00:00) :</span><span class="sxs-lookup"><span data-stu-id="037ce-114">The following command deletes all the device update configuration settings where the log cleanup interval is greater than 10 days (10.00:00:00):</span></span>
    
        Get-CsDeviceUpdateConfiguration | Where-Object {$_.LogCleanUpInterval -gt "10.00:00:00" | Remove-CsDeviceUpdateConfiguration

</div>

<span data-ttu-id="037ce-115">Pour plus d’informations, consultez la rubrique d’aide relative à l’applet de connexion [Remove-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="037ce-115">For details, see the Help topic for the [Remove-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateConfiguration) cmdlet.</span></span>

<span data-ttu-id="037ce-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="037ce-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

