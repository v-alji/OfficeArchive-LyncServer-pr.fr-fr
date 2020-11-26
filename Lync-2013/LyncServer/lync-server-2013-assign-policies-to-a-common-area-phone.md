---
title: 'Lync Server 2013 : attribuer des stratégies à un téléphone de zone commune'
description: 'Lync Server 2013 : attribuez des stratégies à un téléphone de zone commune.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign policies to a common area phone
ms:assetid: f0554fd1-b237-49b3-9eb4-26f4b91f5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994082(v=OCS.15)
ms:contentKeyID: 51803993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe437ec87ba30eff834239db2b4815adb2d5718c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438315"
---
# <a name="assign-policies-in-lync-server-2013-to-a-common-area-phone"></a><span data-ttu-id="26032-103">Attribuer des stratégies dans Lync Server 2013 à un téléphone de zone commune</span><span class="sxs-lookup"><span data-stu-id="26032-103">Assign policies in Lync Server 2013 to a common area phone</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26032-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26032-104">

<span> </span></span></span>

<span data-ttu-id="26032-105">_**Dernière modification de la rubrique :** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="26032-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="26032-106">Après avoir créé votre stratégie de téléphone pour les zones communes (pour plus de détails, voir [créer une stratégie vocale et configurer les enregistrements d’utilisation RTC dans Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), vous pouvez affecter la stratégie à un téléphone réseau commun en utilisant Windows PowerShell et l’applet **de commande Grant-CS** appropriée.</span><span class="sxs-lookup"><span data-stu-id="26032-106">After you create your policy for common area phones (for details, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), you can assign the policy to a common area phone by using Windows PowerShell and the appropriate **Grant-Cs** cmdlet.</span></span> <span data-ttu-id="26032-107">Ces applets de commande peuvent être exécutées à partir de Lync Server 2013 Management Shell ou d’une session distante de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="26032-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="26032-108">Pour plus d’informations sur l’utilisation de Windows PowerShell distant pour vous connecter à Lync Server, voir l’article de blog Lync Server Windows PowerShell « démarrage rapide : gestion de Microsoft Lync Server 2010 à l’aide de Remote PowerShell » [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="26032-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="assigning-a-policy-to-a-single-common-area-phone"></a><span data-ttu-id="26032-109">Attribution d’une stratégie à un seul téléphone standard</span><span class="sxs-lookup"><span data-stu-id="26032-109">Assigning a Policy to a Single Common Area Phone</span></span>

  - <span data-ttu-id="26032-110">La commande suivante affecte le RedmondVoice de la stratégie vocale par utilisateur au téléphone local qui dispose de l’identité bâtiment 14 lobby.</span><span class="sxs-lookup"><span data-stu-id="26032-110">The following command assigns the per-user voice policy RedmondVoice to the common area phone that has the Identity Building 14 Lobby.</span></span>
    
        Grant-CsVoicePolicy -Identity "Building 14 Lobby" -PolicyName "RedmondVoicePolicy"

</div>

<div>

## <a name="assigning-a-policy-to-multiple-common-area-phones"></a><span data-ttu-id="26032-111">Attribution d’une stratégie à plusieurs téléphones de surface commune</span><span class="sxs-lookup"><span data-stu-id="26032-111">Assigning a Policy to Multiple Common Area Phones</span></span>

  - <span data-ttu-id="26032-112">Dans cet exemple, la stratégie vocale RedmondVoice est affectée à l’ensemble des téléphones communs configurés pour une utilisation au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="26032-112">In this example, the per-user voice policy RedmondVoice is assigned to all the common area phones configured for use in the organization.</span></span>
    
        Get-CsCommonAreaPhone | Grant-CsVoicePolicy  -PolicyName "RedmondVoicePolicy"

</div>

<span data-ttu-id="26032-113">Pour plus d’informations, reportez-vous aux rubriques d’aide pour le [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="26032-113">For details, see the Help topics for the [Grant-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsVoicePolicy).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="26032-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26032-114">See Also</span></span>


[<span data-ttu-id="26032-115">Get-CsCommonAreaPhone</span><span class="sxs-lookup"><span data-stu-id="26032-115">Get-CsCommonAreaPhone</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCommonAreaPhone)  
  

<span data-ttu-id="26032-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26032-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

