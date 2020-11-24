---
title: 'Lync Server 2013 : configurer des plages de numéros de capture d’appels de groupe'
description: 'Lync Server 2013 : configurer des plages de numéros de capture d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Group Call Pickup number ranges
ms:assetid: f15f75f6-f965-4558-b612-f40cecdd5d8c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945657(v=OCS.15)
ms:contentKeyID: 51541529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f0594bd681a157b8ff479846b2f6f1964a09cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394784"
---
# <a name="configure-group-call-pickup-number-ranges-in-lync-server-2013"></a><span data-ttu-id="7af1f-103">Configurer des plages de numéros de capture d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7af1f-103">Configure Group Call Pickup number ranges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7af1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7af1f-104">

<span> </span></span></span>

<span data-ttu-id="7af1f-105">_**Dernière modification de la rubrique :** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="7af1f-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="7af1f-106">Le prélèvement d’appels de groupe est basé sur l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="7af1f-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="7af1f-107">Lorsque vous déployez un appel de groupe, vous configurez la table d’orbite du parc d’appels avec des plages de numéros de téléphone désignés comme numéros de groupe de cueillette d’appel.</span><span class="sxs-lookup"><span data-stu-id="7af1f-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="7af1f-108">Ces numéros de groupe sont les numéros que les utilisateurs composent pour prendre des appels qui sonnent pour un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7af1f-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="7af1f-109">Tout comme les numéros d’appels parqués, les numéros de groupe de prise d’appel doivent être des extensions virtuelles auxquelles aucun utilisateur ou téléphone n’est affecté.</span><span class="sxs-lookup"><span data-stu-id="7af1f-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="7af1f-110">Chaque pool frontal sur lequel vous déployez la capture d’appels de groupe peut avoir une ou plusieurs gammes de numéros de groupe de cueillette d’appel.</span><span class="sxs-lookup"><span data-stu-id="7af1f-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="7af1f-111">Les plages de numéros de groupe doivent être globalement uniques dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="7af1f-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7af1f-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7af1f-112">In This Section</span></span>

  - [<span data-ttu-id="7af1f-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7af1f-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

  - [<span data-ttu-id="7af1f-114">Supprimer une plage de numéros de capture d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7af1f-114">Delete a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-delete-a-group-call-pickup-number-range.md)

<span data-ttu-id="7af1f-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7af1f-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

