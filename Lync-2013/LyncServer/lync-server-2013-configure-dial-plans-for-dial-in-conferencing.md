---
title: 'Lync Server 2013 : Configuration des plans de numérotation pour les conférences rendez-vous'
description: 'Lync Server 2013 : configuration de plans de numérotation pour les conférences rendez-vous.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial plans for dial-in conferencing
ms:assetid: a3e0958e-384f-43e5-b4c9-686b6ecac7ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412768(v=OCS.15)
ms:contentKeyID: 48185051
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28123f905288ce35b6f470168962a3d8e6faa22b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395128"
---
# <a name="configure-dial-plans-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="4c300-103">Configuration des plans de numérotation pour les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c300-103">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c300-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c300-104">

<span> </span></span></span>

<span data-ttu-id="4c300-105">_**Dernière modification de la rubrique :** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="4c300-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="4c300-106">Lorsque vous déployez la conférence rendez-vous, vous devez créer ou modifier un ou plusieurs plans de routage des numéros de téléphone d’accès entrant.</span><span class="sxs-lookup"><span data-stu-id="4c300-106">When you deploy dial-in conferencing, you need to create or modify one or more dial plans for routing dial-in access phone numbers.</span></span> <span data-ttu-id="4c300-107">Vérifiez qu’au moins une règle de normalisation dans chaque plan de numérotation convertit les extensions de téléphone en numéros de téléphone valides au format E. 164.</span><span class="sxs-lookup"><span data-stu-id="4c300-107">Make sure that at least one normalization rule in each dial plan converts telephone extensions into complete phone numbers in E.164 format.</span></span> <span data-ttu-id="4c300-108">Les utilisateurs de conférences rendez-vous participent à des conférences en tant qu’utilisateurs d’entreprise authentifiés en entrant leur code confidentiel et leur numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="4c300-108">Users of dial-in conferencing join conferences as authenticated enterprise users by entering their personal identification number (PIN) and their phone number.</span></span> <span data-ttu-id="4c300-109">Vous avez besoin d’une règle de normalisation pour convertir les numéros de poste en numéros de téléphone complets afin que les utilisateurs puissent être authentifiés lorsqu’ils saisissent simplement un numéro de poste.</span><span class="sxs-lookup"><span data-stu-id="4c300-109">You need a normalization rule to convert extensions into complete phone numbers so that users can be authenticated when they enter just a telephone extension.</span></span>

<span data-ttu-id="4c300-110">Pour configurer des plans de numérotation pour la Conférence rendez-vous, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4c300-110">To set up dial plans for dial-in conferencing, do the following:</span></span>

  - <span data-ttu-id="4c300-111">Que vous déployiez ou non Voix Entreprise, modifiez le plan de numérotation global pour ajouter une région de conférence rendez-vous et veillez à ce qu’une règle de normalisation convertisse avec précision vos numéros d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c300-111">Whether or not you deploy Enterprise Voice, modify the global dial plan to add a dial-in conferencing region and to make sure that a normalization rule accurately converts your dial-in access numbers.</span></span> <span data-ttu-id="4c300-112">Pour obtenir des instructions détaillées, voir [modifier un plan de numérotation dans Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="4c300-112">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

  - <span data-ttu-id="4c300-113">Si vous n’avez pas déployé Voix Entreprise, créez des plans de numérotation pour vos numéros d’accès aux conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="4c300-113">If you did not deploy Enterprise Voice, create dial plans for your dial-in conferencing access numbers.</span></span> <span data-ttu-id="4c300-114">Veillez à inclure une région de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="4c300-114">Be sure to include a dial-in conferencing region.</span></span> <span data-ttu-id="4c300-115">Pour obtenir des instructions détaillées, voir [créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="4c300-115">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

  - <span data-ttu-id="4c300-116">Si vous avez déployé Voix Entreprise, modifiez, si nécessaire, les plans de numérotation de Voix Entreprise pour inclure des régions et utilisez les règles de normalisation appropriées pour les numéros d’accès entrant.</span><span class="sxs-lookup"><span data-stu-id="4c300-116">If you deployed Enterprise Voice, modify Enterprise Voice dial plans as necessary to include regions and use appropriate normalization rules for dial-in access numbers.</span></span> <span data-ttu-id="4c300-117">Pour obtenir des instructions détaillées, voir [modifier un plan de numérotation dans Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="4c300-117">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span> <span data-ttu-id="4c300-118">Vous pouvez également créer des plans de numérotation dédiés, utilisés exclusivement pour les numéros d’accès entrant.</span><span class="sxs-lookup"><span data-stu-id="4c300-118">You can also create dedicated dial plans that are used only for dial-in access numbers.</span></span> <span data-ttu-id="4c300-119">Pour obtenir des instructions détaillées, voir [créer un plan de numérotation dans Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="4c300-119">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<span data-ttu-id="4c300-120">Pour plus d’informations sur les régions de planification, voir [exigences relatives aux conférences rendez-vous dans Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="4c300-120">For details about planning regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4c300-121">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4c300-121">In This Section</span></span>

  - [<span data-ttu-id="4c300-122">Afficher les informations de plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c300-122">View dial plan information in Lync Server 2013</span></span>](lync-server-2013-view-dial-plan-information.md)

  - [<span data-ttu-id="4c300-123">Créer un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c300-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)

  - [<span data-ttu-id="4c300-124">Modification d’un plan de numérotation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c300-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)

  - [<span data-ttu-id="4c300-125">Définition de règles de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c300-125">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)

<span data-ttu-id="4c300-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c300-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

