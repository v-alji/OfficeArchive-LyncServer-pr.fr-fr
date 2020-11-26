---
title: 'Lync Server 2013 : Vérification de l’affectation des régions aux plans de numérotation'
description: 'Lync Server 2013 : vérifier que les plans de numérotation ont été attribués.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426150"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="166e0-103">Vérifier que le plan de numérotation Lync Server 2013 a des régions affectées</span><span class="sxs-lookup"><span data-stu-id="166e0-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="166e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="166e0-104">

<span> </span></span></span>

<span data-ttu-id="166e0-105">_**Dernière modification de la rubrique :** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="166e0-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="166e0-106">Les plans de numérotation qui sont utilisés pour les conférences rendez-vous doivent disposer d’une **région de conférence** rendez-vous pour associer les numéros d’accès aux conférences rendez-vous au plan de numérotation approprié.</span><span class="sxs-lookup"><span data-stu-id="166e0-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="166e0-107">Lorsque vous créez un plan de numérotation, vous spécifiez la région de conférence rendez-vous qui s’applique au plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="166e0-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="166e0-108">Lorsque vous créez le numéro d’accès à une conférence rendez-vous, vous sélectionnez les régions qui associent le numéro d’accès aux plans de numérotation appropriés.</span><span class="sxs-lookup"><span data-stu-id="166e0-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="166e0-109">Dans la mesure où il est important de spécifier une région pour tous les plans de numérotation, nous vous conseillons d’utiliser cette procédure pour vérifier que tous les plans de numérotation disposent de régions.</span><span class="sxs-lookup"><span data-stu-id="166e0-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="166e0-110">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="166e0-110">This step is optional.</span></span>

<span data-ttu-id="166e0-111">Utilisez l’applet de connexion **Get-CsDialPlan** pour vérifier si la région est définie pour toutes les offres de numérotation de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="166e0-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="166e0-112">Si ce n’est pas le cas, vous pouvez utiliser l’applet de commande **Set-CsDialPlan** pour configurer la région.</span><span class="sxs-lookup"><span data-stu-id="166e0-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="166e0-113">Vous pouvez également utiliser le panneau de configuration de Lync Server pour mettre à jour la région dans les plans de numérotation existants.</span><span class="sxs-lookup"><span data-stu-id="166e0-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="166e0-114">Pour plus d’informations sur l’utilisation du panneau de configuration de Lync Server, voir [modifier un plan de numérotation dans Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="166e0-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="166e0-115">Pour vérifier que la région est correctement configurée dans les plans de numérotation</span><span class="sxs-lookup"><span data-stu-id="166e0-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="166e0-116">Ouvrez une session sur l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="166e0-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="166e0-117">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="166e0-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="166e0-118">Exécutez la commande suivante dans l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="166e0-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="166e0-119">Exemple :</span><span class="sxs-lookup"><span data-stu-id="166e0-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="166e0-120">Dans cet exemple, tous les plans de numérotation configurés pour votre organisation sont renvoyés.</span><span class="sxs-lookup"><span data-stu-id="166e0-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="166e0-121">Vérifiez les plans de numérotation renvoyés pour identifier ceux ne comportant pas la région de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="166e0-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="166e0-122">Pour plus d’informations, reportez-vous à la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="166e0-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="166e0-123">Pour définir la propriété de région d’un plan de numérotation</span><span class="sxs-lookup"><span data-stu-id="166e0-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="166e0-124">Ouvrez une session sur l’ordinateur en tant que membre du groupe RTCUniversalServerAdmins ou en tant que membre du rôle **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="166e0-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="166e0-125">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="166e0-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="166e0-126">Pour tous les plans de numérotation ne comportant pas de région de conférence rendez-vous, exécutez :</span><span class="sxs-lookup"><span data-stu-id="166e0-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="166e0-127">Exemple :</span><span class="sxs-lookup"><span data-stu-id="166e0-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="166e0-128">Dans cet exemple, le plan de numérotation dont l’identité est Redmond est modifié afin de définir la propriété DialinConferencingRegion sur « US West Coast ».</span><span class="sxs-lookup"><span data-stu-id="166e0-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="166e0-129">Pour plus d’informations, reportez-vous à la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="166e0-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="166e0-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="166e0-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

