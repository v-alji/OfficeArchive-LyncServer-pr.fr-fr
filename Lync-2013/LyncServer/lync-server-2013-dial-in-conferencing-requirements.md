---
title: Configuration requise pour les conférences rendez-vous Lync Server 2013
description: Configuration requise pour les conférences rendez-vous Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing requirements
ms:assetid: 9aff949e-3dac-481a-be46-a180c72e8066
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398802(v=OCS.15)
ms:contentKeyID: 48184969
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0850204993935998c4c098bc7c2866a8a6f3fa1e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429226"
---
# <a name="dial-in-conferencing-requirements-in-lync-server-2013"></a><span data-ttu-id="03b6b-103">Configuration requise pour les conférences rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03b6b-103">Dial-in conferencing requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03b6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03b6b-104">

<span> </span></span></span>

<span data-ttu-id="03b6b-105">_**Dernière modification de la rubrique :** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="03b6b-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="03b6b-106">Avant de démarrer le processus de déploiement de Lync Server 2013, vous devez planifier les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="03b6b-106">Before you start the Lync Server 2013 deployment process you need to plan for the following:</span></span>

  - <span data-ttu-id="03b6b-107">Configuration à utiliser pour la connexion au réseau téléphonique public commuté (RTC)</span><span class="sxs-lookup"><span data-stu-id="03b6b-107">The configuration to use for connecting to the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="03b6b-108">Votre stratégie d’affectation de zones de conférence rendez-vous à des numéros d’accès rendez-vous</span><span class="sxs-lookup"><span data-stu-id="03b6b-108">Your strategy for assigning dial-in conferencing regions to dial-in access numbers</span></span>

  - <span data-ttu-id="03b6b-109">Votre stratégie de création d’annuaires de conférences</span><span class="sxs-lookup"><span data-stu-id="03b6b-109">Your strategy for creating conference directories</span></span>

<div>

## <a name="planning-for-dial-in-pstn-connectivity"></a><span data-ttu-id="03b6b-110">Planification de la connectivité PSTN rendez-vous</span><span class="sxs-lookup"><span data-stu-id="03b6b-110">Planning for Dial-in PSTN Connectivity</span></span>

<span data-ttu-id="03b6b-111">La Conférence rendez-vous requiert au moins un serveur de médiation et au moins une passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="03b6b-111">Dial-in conferencing requires at least one Mediation Server and at least one PSTN gateway.</span></span>

<span data-ttu-id="03b6b-112">Vous pouvez déployer un serveur de médiation dans un site central ou dans un site de succursale.</span><span class="sxs-lookup"><span data-stu-id="03b6b-112">You can deploy a Mediation Server in a central site or in a branch site.</span></span> <span data-ttu-id="03b6b-113">Dans un site central, vous pouvez colocaliser un serveur de médiation sur un pool frontal ou un serveur Standard Edition ou vous pouvez le déployer sur un serveur ou un pool autonome.</span><span class="sxs-lookup"><span data-stu-id="03b6b-113">In a central site, you can collocate a Mediation Server on a Front End pool or Standard Edition server, or you can deploy it on a stand-alone server or pool.</span></span> <span data-ttu-id="03b6b-114">Dans un site de succursale, vous pouvez déployer un serveur de médiation sur un serveur autonome ou comme composant du serveur Survivable Branch Appliance.</span><span class="sxs-lookup"><span data-stu-id="03b6b-114">In a branch site, you can deploy a Mediation Server on a stand-alone server or as a component of the Survivable Branch Appliance.</span></span>

<span data-ttu-id="03b6b-p102">Vous pouvez déployer une passerelle RTC dans un site central ou dans un site de succursale. Dans un site de succursale, la passerelle RTC peut être autonome ou un composant Survivable Branch Appliance.</span><span class="sxs-lookup"><span data-stu-id="03b6b-p102">You can deploy a PSTN gateway in a central site or in a branch site. In a branch site, the PSTN gateway can be stand-alone or a component of the Survivable Branch Appliance.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="03b6b-117">La fonction de conférence rendez-vous n’utilise pas le recours au contenu multimédia, car le serveur de conférence A/V ne prend pas en charge la dérivation multimédia.</span><span class="sxs-lookup"><span data-stu-id="03b6b-117">Dial-in conferencing does not use media bypass because A/V Conferencing Server do not support media bypass.</span></span>



</div>

<span data-ttu-id="03b6b-118">Pour plus d’informations sur la planification de votre configuration du serveur de médiation et des passerelles RTC pour les conférences rendez-vous, voir [composants et topologies du serveur de médiation dans Lync server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="03b6b-118">For details about planning your configuration for Mediation Server and PSTN gateways for dial-in conferencing, see [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

</div>

<span id="bkmk_PlanningforDialinConferencingRegions"></span>

<div>

## <a name="planning-for-dial-in-conferencing-regions"></a><span data-ttu-id="03b6b-119">Planification des régions de conférence rendez-vous</span><span class="sxs-lookup"><span data-stu-id="03b6b-119">Planning for Dial-in Conferencing Regions</span></span>

<span data-ttu-id="03b6b-120">Lors de la configuration d’un rendez-vous, vous créez des plans de numérotation et des numéros d’accès pour les conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="03b6b-120">During dial-in configuration, you create dial plans and dial-in conferencing access numbers.</span></span> <span data-ttu-id="03b6b-121">Le plan de numérotation est un ensemble de règles de normalisation qui spécifient le nombre et le modèle de chiffres d’un numéro de téléphone et traduisant ce numéro de téléphone dans le format E. 164 standard pour le routage des appels.</span><span class="sxs-lookup"><span data-stu-id="03b6b-121">Dial plans are sets of normalization rules that specify the number and pattern of digits in a phone number and translate the phone number into the standard E.164 format for call routing.</span></span> <span data-ttu-id="03b6b-122">Les numéros d’accès aux conférences rendez-vous sont les numéros que les participants composent pour accéder à une conférence.</span><span class="sxs-lookup"><span data-stu-id="03b6b-122">Dial-in conferencing access numbers are the numbers participants call to join a conference.</span></span>

<span data-ttu-id="03b6b-123">Tout numéro d’accès à une conférence rendez-vous doit être associé à au moins un plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="03b6b-123">Every dial-in conferencing access number must be associated with at least one dial plan.</span></span> <span data-ttu-id="03b6b-124">Régions de conférence rendez-vous associez un numéro d’accès à une conférence rendez-vous à ses plans de numérotation.</span><span class="sxs-lookup"><span data-stu-id="03b6b-124">Dial-in conferencing regions associate a dial-in conferencing access number with its dial plans.</span></span> <span data-ttu-id="03b6b-125">Lorsque vous configurez un plan de numérotation, vous spécifiez la région de conférence rendez-vous qui s’applique au plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="03b6b-125">When you set up a dial plan, you specify the dial-in conferencing region that applies to the dial plan.</span></span> <span data-ttu-id="03b6b-126">Quand vous créez le numéro d’accès à la conférence rendez-vous, vous sélectionnez les régions qui associent le numéro d’accès aux plans de numérotation appropriés.</span><span class="sxs-lookup"><span data-stu-id="03b6b-126">When you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="03b6b-127">Lorsque vous créez un plan de numérotation, vous spécifiez l’étendue du plan de numérotation : étendue des utilisateurs, étendue du pool ou étendue du site.</span><span class="sxs-lookup"><span data-stu-id="03b6b-127">When you create a dial plan, you specify the scope of the dial plan: user scope, pool scope, or site scope.</span></span> <span data-ttu-id="03b6b-128">Chaque utilisateur est associé au plan de numérotation dans l’étendue la plus restreinte applicable à son cas.</span><span class="sxs-lookup"><span data-stu-id="03b6b-128">Every user is assigned the dial plan from the narrowest scope that applies to the user.</span></span> <span data-ttu-id="03b6b-129">Par exemple, un utilisateur est affecté à un plan de numérotation de niveau utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="03b6b-129">For example, a user is assigned a user-level dial plan, if one applies.</span></span> <span data-ttu-id="03b6b-130">Si aucun plan de numérotation de niveau utilisateur ne s’applique, l’utilisateur est affecté à un plan de numérotation au niveau du pool.</span><span class="sxs-lookup"><span data-stu-id="03b6b-130">If a user-level dial plan does not apply, the user is assigned a pool-level dial plan.</span></span> <span data-ttu-id="03b6b-131">Si aucun plan de numérotation au niveau du pool ne s’applique, l’utilisateur est affecté à un plan de numérotation au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="03b6b-131">If a pool-level dial plan does not apply, the user is assigned a site-level dial plan.</span></span> <span data-ttu-id="03b6b-132">Si aucun plan de numérotation au niveau du site ne s’applique, l’utilisateur est affecté à un plan de numérotation global.</span><span class="sxs-lookup"><span data-stu-id="03b6b-132">If a site-level dial plan does not apply, the user is assigned the global dial plan.</span></span>

<span data-ttu-id="03b6b-p106">Avant de configurer les plans de numérotation, il est important de planifier le mode d’attribution de nom des régions et l’utilisation des régions. Les considérations suivantes s’appliquent aux régions de conférence rendez-vous :</span><span class="sxs-lookup"><span data-stu-id="03b6b-p106">Before you configure the dial plans, is it important to plan how you want to name and use regions. The following considerations apply to dial-in conferencing regions:</span></span>

  - <span data-ttu-id="03b6b-135">Une région constitue généralement une zone géographique associée à un bureau ou à un groupe de bureaux.</span><span class="sxs-lookup"><span data-stu-id="03b6b-135">A region is typically a geographical area that is associated with an office or group of offices.</span></span>

  - <span data-ttu-id="03b6b-p107">Des langues sont associées aux numéros d’accès aux conférences rendez-vous. Si vous prenez en charge des zones géographiques comprenant plusieurs langues, vous devez déterminer le mode de définition des régions pour prendre en charge les différentes langues. Par exemple, vous pouvez définir différentes régions en associant une zone géographique et une langue ou définir une seule région en fonction de la zone géographique et disposer de différents numéros d’accès aux conférences rendez-vous pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="03b6b-p107">Languages are associated with dial-in access numbers. If you support geographical areas that have multiple languages, you should decide how you want to define regions to support the multiple languages. For example, you might define multiple regions based on a combination of geography and language, or you might define a single region based on geography and have a different dial-in access numbers for each language.</span></span>

  - <span data-ttu-id="03b6b-139">Lorsqu’un utilisateur programme une réunion, par défaut, cette dernière utilise la région spécifiée dans le plan de numérotation de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="03b6b-139">When a user schedules a meeting, by default the meeting uses the region specified by that user's dial plan.</span></span>

  - <span data-ttu-id="03b6b-140">Par défaut, tous les numéros d’accès rendez-vous de la région sont inclus dans l’invitation à la réunion.</span><span class="sxs-lookup"><span data-stu-id="03b6b-140">By default, the all of the dial-in access numbers for the region are included in the meeting invitation.</span></span>

  - <span data-ttu-id="03b6b-141">Il est important de nommer les régions de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="03b6b-141">It is important to name regions so that they are clearly recognizable.</span></span> <span data-ttu-id="03b6b-142">L’utilisateur peut recourir aux noms pour modifier une région de réunion afin que les différents numéros d’accès soient inclus dans l’invitation.</span><span class="sxs-lookup"><span data-stu-id="03b6b-142">The user can use the names of the regions to change a meeting's region so that different access numbers are included in the invitation.</span></span> <span data-ttu-id="03b6b-143">(Lorsque les utilisateurs utilisent Outlook pour planifier une réunion, l’utilisateur utilise le complément réunion en ligne pour Lync 2013 pour modifier la région).</span><span class="sxs-lookup"><span data-stu-id="03b6b-143">(When users use Outlook to schedule a meeting, the user uses the Online Meeting Add-in for Lync 2013 to change the region).</span></span>

  - <span data-ttu-id="03b6b-144">Les régions doivent être désignées de sorte que tout invité souhaitant accéder à une conférence puisse visualiser un numéro d’accès local dans l’invitation.</span><span class="sxs-lookup"><span data-stu-id="03b6b-144">Regions should be designed so that any invitee who wants to dial into a conference can see a local access number in the conference invitation.</span></span>

  - <span data-ttu-id="03b6b-145">Vous pouvez configurer l’ordre dans lequel les numéros d’accès au sein d’une région apparaissent sur la page Paramètres de conférence rendez-vous (et, par conséquent, l’ordre dans lequel ils apparaissent dans l’invitation à la Conférence) en utilisant des applets de commande Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="03b6b-145">You can configure the order in which access numbers within a region appear on the Dial-in Conferencing Settings page (and, therefore, the order in which they appear in the conference invitation) by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="03b6b-146">Un utilisateur peut composer un numéro d’accès pour participer à une conférence rendez-vous en tout point du globe.</span><span class="sxs-lookup"><span data-stu-id="03b6b-146">Any user from any location can call any dial-in access number to join a conference.</span></span>

</div>

<div>

## <a name="planning-for-conference-directories"></a><span data-ttu-id="03b6b-147">Planification des annuaires de conférences</span><span class="sxs-lookup"><span data-stu-id="03b6b-147">Planning for Conference Directories</span></span>

<span data-ttu-id="03b6b-148">Les annuaires de conférences maintiennent un mappage entre l’ID de réunion alphanumérique qu’un participant utilise pour participer à une conférence lors de l’utilisation de la 2013 Lync et l’ID de conférence numérique uniquement qu’un participant à la Conférence rendez-vous utilise pour rejoindre la Conférence.</span><span class="sxs-lookup"><span data-stu-id="03b6b-148">Conference directories maintain a mapping between the alphanumeric meeting ID that a participant uses to join a conference when using Lync 2013, and the numeric-only conference ID that a dial-in conferencing participant uses to join the conference.</span></span> <span data-ttu-id="03b6b-149">Le format de l’ID de conférence est le suivant :</span><span class="sxs-lookup"><span data-stu-id="03b6b-149">The format of the conference ID is as follows:</span></span>

    <housekeeping digit (1 digit)><conference directory (usually 1-2 digits)><conference number (variable number of digits><check digit (1 digit)>

<span data-ttu-id="03b6b-150">La création de différents annuaires des conférences permet de s’assurer que les ID de conférences restent courts jusqu’à ce qu’une quantité importante de conférences ait été créée.</span><span class="sxs-lookup"><span data-stu-id="03b6b-150">Creating multiple conference directories will ensure that conference IDs will stay short until a significant amount of conferences have been created.</span></span> <span data-ttu-id="03b6b-151">Dans une organisation avec un nombre type de conférences par utilisateur, il est recommandé de créer un annuaire des conférences ne dépassant pas 999 utilisateurs dans le pool.</span><span class="sxs-lookup"><span data-stu-id="03b6b-151">In an organization with a typical number of conferences per user, we recommend that you create one conference directory for every 999 users in the pool.</span></span> <span data-ttu-id="03b6b-152">Dans cette règle, les ID de conférence peuvent généralement être conservés de petite taille.</span><span class="sxs-lookup"><span data-stu-id="03b6b-152">Using this guideline the conference IDs can generally be kept small.</span></span> <span data-ttu-id="03b6b-153">Cependant, lorsque le nombre d’annuaires de conférences (tous pools confondus) dépasse 9, la longueur de l’ID de conférence augmente pour permettre la prise en charge de conférences supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="03b6b-153">However, once the number of conference directories (across the pools) exceed 9, the Conference ID number will grow to support additional conferences.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="03b6b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b6b-154">See Also</span></span>


[<span data-ttu-id="03b6b-155">Composant serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03b6b-155">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  
[<span data-ttu-id="03b6b-156">Plans de numérotation et règles de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="03b6b-156">Dial plans and normalization rules in Lync Server 2013</span></span>](lync-server-2013-dial-plans-and-normalization-rules.md)  
  

<span data-ttu-id="03b6b-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03b6b-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

