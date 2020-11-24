---
title: 'Lync Server 2013 : vérifier les règles de normalisation du parc d’appels'
description: 'Lync Server 2013 : vérifier les règles de normalisation du parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395033"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a><span data-ttu-id="6b7a3-103">Vérifier les règles de normalisation du parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7a3-103">Verify normalization rules for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b7a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b7a3-104">

<span> </span></span></span>

<span data-ttu-id="6b7a3-105">_**Dernière modification de la rubrique :** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="6b7a3-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="6b7a3-106">Le parking des orbites ne doit pas être normalisé.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-106">Call Park orbits must not be normalized.</span></span> <span data-ttu-id="6b7a3-107">Vérifiez dans vos plans de numérotation que vos numéros orbites ne sont pas normalisés.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span></span> <span data-ttu-id="6b7a3-108">Si vous devez créer une règle de normalisation supplémentaire pour empêcher la normalisation de vos orbites, suivez la procédure décrite dans la rubrique [créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md) pour définir une nouvelle règle de normalisation, afin que le **modèle correspondant** identifie la plage d’orbite et le **modèle de traduction** est **$1**.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-108">If you must create an additional normalization rule to prevent your orbits from being normalized, follow the procedure in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) to define a new normalization rule, so that **Pattern to match** identifies the orbit range and **Translation pattern** is **$1**.</span></span> <span data-ttu-id="6b7a3-109">Par exemple, si la plage de votre stationnement d’appels est 7000 – 7999, le **modèle à faire correspondre** est **^ (7 \\ d {3} ) $** et le **modèle de traduction** est **$1**.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-109">For example, if your Call Park orbit range is 7000 – 7999, the **Pattern to match** is **^(7\\d{3})$** and **Translation pattern** is **$1**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6b7a3-110">Vérifiez que la règle de normalisation par défaut de vos plans de numérotation ne contient pas l’élément <STRONG>^(\d\*)</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span></span> <span data-ttu-id="6b7a3-111">Dans le cas contraire, votre règle de normalisation de parc d’appels ne sera jamais exécutée.</span><span class="sxs-lookup"><span data-stu-id="6b7a3-111">Otherwise, your Call Park normalization rule will never run.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6b7a3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b7a3-112">See Also</span></span>


[<span data-ttu-id="6b7a3-113">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7a3-113">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
  

<span data-ttu-id="6b7a3-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b7a3-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

