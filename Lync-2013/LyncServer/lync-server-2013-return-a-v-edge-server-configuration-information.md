---
title: 'Lync Server 2013 : renvoi des informations de configuration de serveur Edge A/V'
description: 'Lync Server 2013 : renvoi des informations de configuration de serveur Edge A/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Return A/V Edge Server configuration information
ms:assetid: b041f5a4-2387-4075-846c-ec4f99640903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721850(v=OCS.15)
ms:contentKeyID: 49733783
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4f72fccfe51b946dc0dc285aee12a07e59c844b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442473"
---
# <a name="return-av-edge-server-configuration-information-in-lync-server-2013"></a><span data-ttu-id="e1b80-103">Renvoyer des informations de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b80-103">Return A/V Edge Server configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e1b80-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e1b80-104">

<span> </span></span></span>

<span data-ttu-id="e1b80-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="e1b80-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="e1b80-106">Le service Edge A/V offre aux utilisateurs internes (qui sont connectés à votre réseau d’entreprise) un moyen de partager des fichiers audio et vidéo avec des utilisateurs externes (les utilisateurs qui ne sont pas connectés au réseau de votre organisation).</span><span class="sxs-lookup"><span data-stu-id="e1b80-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="e1b80-107">Le service Edge A/V est essentiellement géré à l’aide des paramètres de configuration d’un serveur à l’aide d’une/V, le paramétrage qui peut être configuré sur l’étendue du site ou au niveau de l’étendue de service (autrement dit, peut être configuré pour un serveur Edge A/V individuel).</span><span class="sxs-lookup"><span data-stu-id="e1b80-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="e1b80-108">Pour renvoyer des informations sur les paramètres de configuration de l’utilisation A/V du cadre de votre organisation, vous devez utiliser Windows PowerShell et l’applet de Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1b80-108">To return information about the A/V Edge configuration settings in use in your organization, you must use Windows PowerShell and the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="e1b80-109">Pour plus d’informations, consultez la rubrique d’aide de l’applet de passe [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="e1b80-109">For more information, see the help topic for the [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet.</span></span>

<span data-ttu-id="e1b80-110">Les informations renvoyées par l’applet de requête Get-CsAVEdgeConfiguration se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1b80-110">Information returned from the Get-CsAVEdgeConfiguration cmdlet will look similar to this:</span></span>

    Identity              : Global
    MaxTokenLifetime      : 08:00:00
    MaxBandwidthPerUserKb : 10000
    MaxBandwidthPerPortKb : 3000

<div>

## <a name="to-return-information-for-all-your-av-edge-configuration-settings"></a><span data-ttu-id="e1b80-111">Pour renvoyer des informations pour tous les paramètres de configuration de Microsoft A/V Edge</span><span class="sxs-lookup"><span data-stu-id="e1b80-111">To return information for all your A/V Edge configuration settings</span></span>

  - <span data-ttu-id="e1b80-112">La commande suivante renvoie des informations sur l’ensemble des paramètres de configuration d’une bordure A/V actuellement utilisés au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="e1b80-112">The following command returns information about all the A/V Edge configuration settings currently in use in your organization:</span></span>
    
        Get-CsAVEdgeConfiguration

</div>

<div>

## <a name="to-return-information-for-site-scoped-av-edge-configuration-settings"></a><span data-ttu-id="e1b80-113">Pour renvoyer des informations sur les paramètres de configuration de périmètre A/V d’une application de site</span><span class="sxs-lookup"><span data-stu-id="e1b80-113">To return information for site-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="e1b80-114">Pour renvoyer des informations sur une collection spécifique de paramètres de configuration de bord A/V, spécifiez l’identité de cette collection lorsque vous exécutez l’applet de cmdlet Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e1b80-114">To return information about a specific collection of A/V Edge configuration settings, specify the Identity of that collection when running the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="e1b80-115">Par exemple, cette commande renvoie uniquement des informations sur les paramètres appliqués au site de Redmond :</span><span class="sxs-lookup"><span data-stu-id="e1b80-115">For example, this command returns information only for the settings applied to the Redmond site:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-return-information-for-service-scoped-av-edge-configuration-settings"></a><span data-ttu-id="e1b80-116">Pour renvoyer des informations sur les paramètres de configuration de périmètre d’une application de service A/V</span><span class="sxs-lookup"><span data-stu-id="e1b80-116">To return information for service-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="e1b80-117">Cette commande renvoie des informations uniquement pour les paramètres appliqués à un serveur Edge A/V spécifique.</span><span class="sxs-lookup"><span data-stu-id="e1b80-117">And this command returns information only for settings applied the a specific A/V Edge server:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e1b80-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1b80-118">See Also</span></span>


[<span data-ttu-id="e1b80-119">Créer ou modifier un ensemble de paramètres de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b80-119">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  
[<span data-ttu-id="e1b80-120">Supprimer une collection existante de paramètres de configuration de serveur Edge A/V dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b80-120">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="e1b80-121">Serveurs périphériques audio/vidéo (A/V) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e1b80-121">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
  

<span data-ttu-id="e1b80-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e1b80-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

