---
title: 'Lync Server 2013 : supprimer une plage de numéros de capture d’appels de groupe'
description: 'Lync Server 2013 : supprimer une plage de numéros de capture d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Group Call Pickup number range
ms:assetid: 521891f3-7a5d-45de-92dc-d57025453159
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945629(v=OCS.15)
ms:contentKeyID: 51541475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b40d423b64d29300741c55433864128897c3ac8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430706"
---
# <a name="delete-a-group-call-pickup-number-range-in-lync-server-2013"></a><span data-ttu-id="3f661-103">Supprimer une plage de numéros de capture d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f661-103">Delete a Group Call Pickup number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f661-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f661-104">

<span> </span></span></span>

<span data-ttu-id="3f661-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="3f661-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="3f661-106">Utilisez la procédure suivante pour supprimer une plage de numéros de capture d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="3f661-106">Use the following procedure to delete a Group Call Pickup number range.</span></span>

<div>

## <a name="to-delete-a-call-pickup-group-number-range"></a><span data-ttu-id="3f661-107">Pour supprimer une plage de numéros de groupe de collecte d’appels</span><span class="sxs-lookup"><span data-stu-id="3f661-107">To delete a call pickup group number range</span></span>

1.  <span data-ttu-id="3f661-108">Ouvrez une session sur l’ordinateur sur lequel Lync Server Management Shell est installé en tant que membre du groupe RTCUniversalServerAdmins ou avec les droits d’utilisateur nécessaires, comme décrit dans la rubrique [autorisations de configuration du délégué dans Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="3f661-108">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="3f661-109">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="3f661-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3f661-110">Dans la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="3f661-110">At the command line, type:</span></span>
    
        Remove-CsCallParkOrbit -Identity "<group number range name>" 
    
    <span data-ttu-id="3f661-111">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3f661-111">For example:</span></span>
    
        Remove-CsCallParkOrbit -Identity "Redmond call pickup"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3f661-112">Pour plus d’informations sur les autres options, voir <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="3f661-112">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f661-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f661-113">See Also</span></span>


[<span data-ttu-id="3f661-114">Créer ou modifier une gamme de parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f661-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[<span data-ttu-id="3f661-115">Remove-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="3f661-115">Remove-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[<span data-ttu-id="3f661-116">Get-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="3f661-116">Get-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

<span data-ttu-id="3f661-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f661-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

