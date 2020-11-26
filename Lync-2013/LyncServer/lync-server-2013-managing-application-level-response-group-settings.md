---
title: 'Lync Server 2013 : gestion des paramètres de groupe de réponse au niveau de l’application'
description: 'Lync Server 2013 : gestion des paramètres de groupe de réponse au niveau de l’application.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing application-level Response Group settings
ms:assetid: aab749a1-fa2d-4ce8-a6c6-ebcfa37ce02a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721843(v=OCS.15)
ms:contentKeyID: 49733776
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd362cbe8ce738a16639b89edd79439b564444ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425996"
---
# <a name="managing-application-level-response-group-settings-in-lync-server-2013"></a><span data-ttu-id="f067c-103">Gestion des paramètres du groupe de réponses au niveau de l’application dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f067c-103">Managing application-level Response Group settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f067c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f067c-104">

<span> </span></span></span>

<span data-ttu-id="f067c-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f067c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f067c-106">Les paramètres au niveau de l’application de l’application Response Group incluent la configuration par défaut de l’attente de musique, le fichier audio de musique par défaut, la période de grâce aux retours de l’agent et la configuration du contexte d’appel.</span><span class="sxs-lookup"><span data-stu-id="f067c-106">Application-level settings for Response Group application include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="f067c-107">Vous pouvez définir un seul ensemble de paramètres de niveau application par pool.</span><span class="sxs-lookup"><span data-stu-id="f067c-107">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="f067c-108">Pour afficher les paramètres de niveau application, utilisez l’applet de commande **Get-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f067c-108">To view application-level settings, use the **Get-CsRgsConfiguration** cmdlet.</span></span> <span data-ttu-id="f067c-109">Pour modifier les paramètres de niveau application, utilisez l’applet de commande **Set-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f067c-109">To modify the application-level settings, use the **Set-CsRgsConfiguration** cmdlet.</span></span>

<span data-ttu-id="f067c-p102">L’attente musicale par défaut est lue lorsqu’un appel est mis en attente uniquement si aucune attente musicale personnalisée n’est définie. Le contexte de l’appel est disponible uniquement pour les files d’attentes assignées à des flux de travail interactifs. Si le contexte de l’appel est activé, un agent peut afficher des informations telles que le délai d’attente de l’appelant ou des questions et réponses de flux de travail lorsqu’un appel est reçu.</span><span class="sxs-lookup"><span data-stu-id="f067c-p102">The default music on hold is played when a call is placed on hold only if no custom music on hold is defined. Call context is available only for queues assigned to interactive workflows. If call context is enabled, an agent can see information such as caller wait time or workflow questions and answers when the call is received.</span></span>

<div>

## <a name="to-modify-response-group-application-level-settings"></a><span data-ttu-id="f067c-113">Pour modifier les paramètres au niveau de l’application de Response Group</span><span class="sxs-lookup"><span data-stu-id="f067c-113">To modify Response Group application-level settings</span></span>

1.  <span data-ttu-id="f067c-114">Ouvrez une session en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre de l’un des rôles d’administration prédéfinis prenant en charge Response Group.</span><span class="sxs-lookup"><span data-stu-id="f067c-114">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="f067c-115">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f067c-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f067c-116">Dans la ligne de commande, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f067c-116">At the command line, run:</span></span>
    
        Set-CsRgsConfiguration -Identity <name of service hosting Response Group> [-AgentRingbackGracePeriod <# seconds until call returns to agent after declined>] [-DefaultMusicOnHoldFile <audio file>] [-DisableCallContext <$true | $false>]
    
    <span data-ttu-id="f067c-117">Exemple :</span><span class="sxs-lookup"><span data-stu-id="f067c-117">For example:</span></span>
    
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -AgentRingbackGracePeriod 30 -DisableCallContext $false
    
    <span data-ttu-id="f067c-p103">Pour spécifier un fichier audio à utiliser comme attente musicale par défaut, vous devez d’abord importer le fichier audio. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f067c-p103">To specify an audio file to use as the default music on hold, you need to import the audio file first. For example:</span></span>
    
        $x = Import-CsRgsAudioFile -Identity "service:ApplicationServer:redmond.contoso.com" -FileName "MusicWhileYouWait.wav" -Content (Get-Content C:\Media\ MusicWhileYouWait.wav -Encoding byte -ReadCount 0)
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -DefaultMusicOnHoldFile <$x>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f067c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f067c-120">See Also</span></span>


[<span data-ttu-id="f067c-121">Get-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f067c-121">Get-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration)  
[<span data-ttu-id="f067c-122">Set-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f067c-122">Set-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsConfiguration)  
[<span data-ttu-id="f067c-123">Importation-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="f067c-123">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
  

<span data-ttu-id="f067c-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f067c-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

