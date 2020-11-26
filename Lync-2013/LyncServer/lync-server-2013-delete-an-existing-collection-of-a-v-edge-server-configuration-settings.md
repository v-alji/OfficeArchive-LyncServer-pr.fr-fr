---
title: Supprimer une collection existante de paramètres de configuration de serveur Edge A/V
description: Supprimez une collection existante de paramètres de configuration de serveur Edge A/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of A/V Edge Server configuration settings
ms:assetid: 668d3613-e464-4b68-967a-cfff90b9ce4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688077(v=OCS.15)
ms:contentKeyID: 49733673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7fe444e8bcb7e7e8e2633e59c23aeb2e80e9b98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430573"
---
# <a name="delete-an-existing-collection-of-av-edge-server-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="1d84d-103">Supprimer une collection existante de paramètres de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d84d-103">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d84d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d84d-104">

<span> </span></span></span>

<span data-ttu-id="1d84d-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="1d84d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="1d84d-106">Le service Edge A/V offre aux utilisateurs internes (qui sont connectés à votre réseau d’entreprise) un moyen de partager des fichiers audio et vidéo avec des utilisateurs externes (les utilisateurs qui ne sont pas connectés au réseau de votre organisation).</span><span class="sxs-lookup"><span data-stu-id="1d84d-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="1d84d-107">Le service Edge A/V est essentiellement géré à l’aide des paramètres de configuration d’un serveur à l’aide d’une/V, le paramétrage qui peut être configuré sur l’étendue du site ou au niveau de l’étendue de service (autrement dit, peut être configuré pour un serveur Edge A/V individuel).</span><span class="sxs-lookup"><span data-stu-id="1d84d-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="1d84d-108">Lorsque vous installez Lync Server, une collection globale des paramètres de configuration de Microsoft Edge a/V est créée pour vous.</span><span class="sxs-lookup"><span data-stu-id="1d84d-108">When you install Lync Server, a global collection of A/V Edge configuration settings is created for you.</span></span> <span data-ttu-id="1d84d-109">Cette collection globale ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="1d84d-109">This global collection cannot be deleted.</span></span> <span data-ttu-id="1d84d-110">Toutefois, vous pouvez utiliser Windows PowerShell et l’applet de Remove-CsAVEdgeConfiguration pour « réinitialiser » la collection globale. Cela signifie simplement que toutes les valeurs de propriété de la collection globale seront réinitialisées à leur valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d84d-110">However, you can use the Windows PowerShell and the Remove-CsAVEdgeConfiguration cmdlet to "reset" the global collection; that simply means that all the property values in the global collection will be reset to their default value.</span></span> <span data-ttu-id="1d84d-111">Par exemple, si vous avez défini la propriété MaxTokenLifetime pendant 16 heures, cette propriété sera réinitialisée sur sa valeur par défaut de 8 heures.</span><span class="sxs-lookup"><span data-stu-id="1d84d-111">For example, if you have set the MaxTokenLifetime property for 16 hours, that property will be reset to its default value of 8 hours.</span></span>

<span data-ttu-id="1d84d-112">Toutefois, les collections de paramètres personnalisés que vous avez créés à l’étendue du site ou l’étendue du service peuvent être supprimées à l’aide de l’applet de applet de Remove-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1d84d-112">However, custom settings collections that you have created at either the site scope or the service scope can be deleted by using the Remove-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="1d84d-113">Si vous supprimez les paramètres du site, les serveurs Edge A/V de ce site seront gérés par les paramètres globaux.</span><span class="sxs-lookup"><span data-stu-id="1d84d-113">If you delete site settings then A/V Edge servers in that site will be managed by the global settings.</span></span> <span data-ttu-id="1d84d-114">Si vous supprimez les paramètres d’étendue des services, ce serveur est alors géré par ses paramètres de site, le cas échéant, ou par les paramètres globaux si aucun paramètre de site n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="1d84d-114">If you delete service-scope settings,, that server will then be managed by its site settings, if they exist, or by the global settings if no site settings are available.</span></span>

<span data-ttu-id="1d84d-115">Pour plus d’informations, reportez-vous à la rubrique d’aide relative à l’applet de passe [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="1d84d-115">For more information, see the help topic for the [Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15)) cmdlet.</span></span>

<div>

## <a name="to-reset-the-global-collection"></a><span data-ttu-id="1d84d-116">Pour réinitialiser la collection globale</span><span class="sxs-lookup"><span data-stu-id="1d84d-116">To reset the global collection</span></span>

  - <span data-ttu-id="1d84d-117">La commande suivante réinitialise la collection globale des paramètres de configuration de Edge A/V :</span><span class="sxs-lookup"><span data-stu-id="1d84d-117">The following command resets the global collection of A/V Edge configuration settings:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "global"

</div>

<div>

## <a name="to-remove-a-collection-from-the-site-scope"></a><span data-ttu-id="1d84d-118">Pour supprimer une collection de l’étendue du site</span><span class="sxs-lookup"><span data-stu-id="1d84d-118">To remove a collection from the site scope</span></span>

  - <span data-ttu-id="1d84d-119">Cette commande supprime les paramètres de configuration d’une application A/V appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="1d84d-119">This command removes the A/V Edge configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-a-collection-from-the-service-scope"></a><span data-ttu-id="1d84d-120">Pour supprimer une collection de l’étendue du service</span><span class="sxs-lookup"><span data-stu-id="1d84d-120">To remove a collection from the service scope</span></span>

  - <span data-ttu-id="1d84d-121">Cette commande supprime les paramètres appliqués au serveur Edge A/V atl-edge-001.litwareinc.com :</span><span class="sxs-lookup"><span data-stu-id="1d84d-121">This command removes the settings applied to the A/V Edge server atl-edge-001.litwareinc.com:</span></span>
    
        Remove-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1d84d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d84d-122">See Also</span></span>


[<span data-ttu-id="1d84d-123">Renvoyer des informations de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d84d-123">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)  
[<span data-ttu-id="1d84d-124">Créer ou modifier un ensemble de paramètres de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d84d-124">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="1d84d-125">Serveurs périphériques audio/vidéo (A/V) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d84d-125">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
<span data-ttu-id="1d84d-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="1d84d-126">[Remove-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg398786(v=OCS.15))</span></span>  
  

<span data-ttu-id="1d84d-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d84d-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

