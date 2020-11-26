---
title: 'Lync Server 2013 : plans de numérotation et règles de normalisation'
description: 'Lync Server 2013 : plans de numérotation et règles de normalisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial plans and normalization rules
ms:assetid: fde45195-6eb4-403c-9094-57df7fc0bd2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413082(v=OCS.15)
ms:contentKeyID: 48185960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0341d0c5267a2272ff45bd93408b2bd14f0ceeaa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429209"
---
# <a name="dial-plans-and-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="0b251-103">Plans de numérotation et règles de normalisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b251-103">Dial plans and normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b251-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b251-104">

<span> </span></span></span>

<span data-ttu-id="0b251-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0b251-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0b251-106">Un plan de numérotation est un ensemble nommé de règles de normalisation qui convertissent des numéros de téléphone pour un emplacement, un utilisateur individuel ou un objet contact nommé, en un format standard (E.164) à des fins d’autorisation téléphonique et de routage des appels.</span><span class="sxs-lookup"><span data-stu-id="0b251-106">A dial plan is a named set of normalization rules that translates phone numbers for a named location, individual user, or contact object into a single standard (E.164) format for purposes of phone authorization and call routing.</span></span>

<span data-ttu-id="0b251-p101">Les règles de normalisation définissent la façon dont les numéros de téléphone exprimés en divers formats sont routés vers chaque emplacement, utilisateur ou objet contact. La même chaîne de numérotation peut être interprétée et convertie différemment selon l’emplacement d’origine de la numérotation et la personne ou l’objet contact passant l’appel.</span><span class="sxs-lookup"><span data-stu-id="0b251-p101">Normalization rules define how phone numbers expressed in various formats are to be routed for each specified location, user, or contact object. The same dial string may be interpreted and translated differently, depending on the location from which it is dialed and the person or contact object making the call.</span></span>

<div>

## <a name="dial-plan-scope"></a><span data-ttu-id="0b251-109">Étendue du plan de numérotation</span><span class="sxs-lookup"><span data-stu-id="0b251-109">Dial Plan Scope</span></span>

<span data-ttu-id="0b251-110">L’*étendue* d’un plan de numérotation détermine le niveau hiérarchique auquel le plan de numérotation peut être appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b251-110">A dial plan’s *scope* determines the hierarchical level at which the dial plan can be applied.</span></span> <span data-ttu-id="0b251-111">Dans Lync Server, un utilisateur peut se voir attribuer un plan de numérotation spécifique par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b251-111">In Lync Server, a user can be assigned a specific per-user dial plan.</span></span> <span data-ttu-id="0b251-112">Si aucun plan de numérotation utilisateur n’est attribué, le plan de numérotation du pool d’inscriptions est appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b251-112">If a user dial plan is not assigned, the Registrar pool dial plan is applied.</span></span> <span data-ttu-id="0b251-113">S’il n’y a pas de plan de numérotation de bureaux d’enregistrement, le plan de numérotation de site est appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b251-113">If there is no Registrar pool dial plan, the site dial plan is applied.</span></span> <span data-ttu-id="0b251-114">Enfin, si aucun autre plan de numérotation ne peut être appliqué à l’utilisateur, le plan de numérotation global est appliqué.</span><span class="sxs-lookup"><span data-stu-id="0b251-114">Finally, if there is no other dial plan applicable to the user, the global dial plan is applied.</span></span>

<span data-ttu-id="0b251-115">Les clients obtiennent les niveaux d’étendue du plan de numérotation via les paramètres de mise en service in-band qui sont fournis lorsque les utilisateurs se connectent à Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b251-115">Clients obtain dial plan scope levels through in-band provisioning settings that are provided when users log on to Lync Server.</span></span> <span data-ttu-id="0b251-116">En tant qu’administrateur, vous pouvez gérer et affecter des niveaux d’étendue de plan de numérotation en utilisant le panneau de configuration de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0b251-116">As the administrator, you can manage and assign dial plan scope levels by using Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0b251-117">Le plan de numérotation de la passerelle PSTN au niveau du service est appliqué aux appels entrant depuis une passerelle donnée.</span><span class="sxs-lookup"><span data-stu-id="0b251-117">The service level public switched telephone network (PSTN) gateway dial plan is applied to the incoming calls from a particular gateway.</span></span>



</div>

<span data-ttu-id="0b251-118">Les niveaux d’étendue du plan de numérotation sont définis comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b251-118">Dial plan scope levels are defined as follows:</span></span>

  - <span data-ttu-id="0b251-119">**Plan de numérotation utilisateur :** Peuvent être attribués à des utilisateurs, des groupes ou des objets de contact individuels.</span><span class="sxs-lookup"><span data-stu-id="0b251-119">**User dial plan:** Can be assigned to individual users, groups, or contact objects.</span></span> <span data-ttu-id="0b251-120">Les applications vocales peuvent chercher un plan de numérotation par utilisateur lors de la réception d’un appel avec le contexte du téléphone défini sur la valeur par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b251-120">Voice applications can look up a per-user dial plan when a call is received with the phone-context set to user-default.</span></span> <span data-ttu-id="0b251-121">Dans le cadre de l’attribution d’un plan de numérotation, un objet contact est considéré comme un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="0b251-121">For the purpose of assigning a dial plan, a contact object is treated as an individual user.</span></span>

  - <span data-ttu-id="0b251-122">**Plan de numérotation de la liste :** Peut être créé au niveau de service pour n’importe quelle passerelle PSTN ou bureau d’enregistrement dans votre topologie.</span><span class="sxs-lookup"><span data-stu-id="0b251-122">**Pool dial plan:** Can be created at the service level for any PSTN gateway or Registrar in your topology.</span></span> <span data-ttu-id="0b251-123">Pour définir un plan de numérotation de groupe, vous devez spécifier le service spécifique (passerelle PSTN ou pool de bureau d’enregistrement) auquel s’applique le plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-123">To define a pool dial plan, you must specify the particular service (PSTN gateway or Registrar pool) to which the dial plan applies.</span></span>

  - <span data-ttu-id="0b251-124">**Plan de numérotation de site :** Peuvent être créés pour un site entier, à l’exception de tous les utilisateurs, groupes ou objets de contact auxquels un plan de numérotation de groupe ou un plan de numérotation est attribué.</span><span class="sxs-lookup"><span data-stu-id="0b251-124">**Site dial plan:** Can be created for an entire site, except for any users, groups, or contact objects that are assigned a pool dial plan or user dial plan.</span></span> <span data-ttu-id="0b251-125">Pour définir un plan de numérotation de site, vous devez spécifier le site auquel s’applique le plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-125">To define a site dial plan, you must specify the site to which the dial plan applies.</span></span>

  - <span data-ttu-id="0b251-126">**Plan de numérotation globale :** Plan de numérotation par défaut installé avec le produit.</span><span class="sxs-lookup"><span data-stu-id="0b251-126">**Global dial plan:** The default dial plan installed with the product.</span></span> <span data-ttu-id="0b251-127">Vous pouvez modifier le plan de numérotation global, mais vous ne pouvez pas le supprimer.</span><span class="sxs-lookup"><span data-stu-id="0b251-127">You can edit the global dial plan, but you cannot delete it.</span></span> <span data-ttu-id="0b251-128">Ce plan de numérotation s’applique à tous les utilisateurs, à tous les groupes et aux objets de contact Enterprise Voice dans votre déploiement, sauf si vous configurez et attribuez un plan de numérotation avec une étendue plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="0b251-128">This dial plan applies to all Enterprise Voice users, groups, and contact objects in your deployment, unless you configure and assign a dial plan with a more specific scope.</span></span>

</div>

<div>

## <a name="planning-for-dial-plans"></a><span data-ttu-id="0b251-129">Planification des plans de numérotation</span><span class="sxs-lookup"><span data-stu-id="0b251-129">Planning for Dial Plans</span></span>

<span data-ttu-id="0b251-130">Pour planifier un plan de numérotation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b251-130">To plan a dial plan, follow these steps:</span></span>

  - <span data-ttu-id="0b251-131">Répertoriez tous les paramètres régionaux dans lesquels votre organisation a un bureau.</span><span class="sxs-lookup"><span data-stu-id="0b251-131">List all the locales in which your organization has an office.</span></span>
    
    <span data-ttu-id="0b251-p108">Cette liste doit être à jour et complète. Elle doit être revue à mesure que la société ou l’organisation évolue. Dans une multinationale de grande taille avec de nombreuses petites succursales, cette tâche peut nécessiter un certain temps.</span><span class="sxs-lookup"><span data-stu-id="0b251-p108">The list must be up-to-date and complete. It will need to be revised as company organization evolves. In a large, multinational company with numerous small branch offices, this can be a time-consuming task.</span></span>

  - <span data-ttu-id="0b251-135">Identifiez des modèles de numéro valides pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="0b251-135">Identify valid number patterns for each site.</span></span>
    
    <span data-ttu-id="0b251-p109">La partie de la planification de vos plans de numérotation qui prend le plus de temps est l’identification des modèles de numéro valides pour chaque site. Dans certains cas, vous pouvez être en mesure de copier les règles de normalisation que vous avez écrites pour un plan de numérotation vers d’autres plan, particulièrement si les site correspondants se trouvent dans les mêmes pays/région ou continent. Dans d’autres cas, de petites modifications apportées aux numéros d’un plan de numérotation peuvent être suffisantes pour permettre leur utilisation dans d’autres plans de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-p109">The most time-consuming part of planning your dial plans is identifying the valid number patterns for each site. In some cases, you may be able to copy normalization rules that you have written for one dial plan to other dial plans, especially if the corresponding sites are within the same country/region or even continent. In other cases, small changes to numbers in one dial plan may be enough to use them in other dial plans.</span></span>

  - <span data-ttu-id="0b251-139">Développez un schéma à l’échelle de l’organisation pour nommer les plans de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-139">Develop an organization-wide scheme for naming dial plans.</span></span>
    
    <span data-ttu-id="0b251-140">L’adoption d’un schéma d’appellation standard assure une cohérence à l’échelle de l’organisation et facilite la maintenance et les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0b251-140">Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.</span></span>

  - <span data-ttu-id="0b251-141">Déterminez la nécessité de plusieurs plans de numérotation pour un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="0b251-141">Decide whether multiple dial plans are required for a single location.</span></span>
    
    <span data-ttu-id="0b251-142">Si votre organisation maintient un seul plan de numérotation sur plusieurs emplacements, vous devrez éventuellement créer un plan de numérotation distinct pour les utilisateurs de la voix entreprise qui effectuent la migration à partir d’un système PBX (Private Branch Exchange) et qui doivent conserver leurs extensions existantes.</span><span class="sxs-lookup"><span data-stu-id="0b251-142">If your organization maintains a single dial plan across multiple locations, you may still need to create a separate dial plan for Enterprise Voice users who are migrating from a private branch exchange (PBX) and who need to have their existing extensions retained.</span></span>

  - <span data-ttu-id="0b251-143">Déterminez la nécessité de plans de numérotation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b251-143">Decide whether per-user dial plans are required.</span></span> <span data-ttu-id="0b251-144">Par exemple, si vous avez des utilisateurs dans un site de succursale qui sont inscrits auprès du site central ou si certains de vos utilisateurs sont inscrits sur une unité de succursale survivant, vous pouvez utiliser des scénarios de numérotation spéciaux pour ces utilisateurs à l’aide de plans de numérotation par utilisateur et de règles de normalisation.</span><span class="sxs-lookup"><span data-stu-id="0b251-144">For example, if you have users at a branch site who are registered with the central site or if you have users who are registered on a Survivable Branch Appliance, you can consider special dialing scenarios for such users using per-user dial plans and normalization rules.</span></span> <span data-ttu-id="0b251-145">Pour plus d’informations, reportez-vous à [Configuration requise pour la résilience de site de succursale pour Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b251-145">For details, see [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).</span></span>

  - <span data-ttu-id="0b251-146">Déterminez l’étendue d’un plan de numérotation (tel que décrit plus haut dans cette rubrique).</span><span class="sxs-lookup"><span data-stu-id="0b251-146">Determine dial plan scope (as previously described in this topic).</span></span>

<span data-ttu-id="0b251-147">Pour créer un plan de numérotation, vous devez spécifier les valeurs dans les champs suivants, le cas échéant, à l’aide du panneau de configuration de Lync Server ou de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="0b251-147">To create a dial plan, you specify values in the following fields, as required, by using Lync Server Control Panel or Lync Server Management Shell.</span></span>

<div>

## <a name="name-and-simple-name"></a><span data-ttu-id="0b251-148">Nom et nom simple</span><span class="sxs-lookup"><span data-stu-id="0b251-148">Name and Simple Name</span></span>

<span data-ttu-id="0b251-149">Pour les plans de numérotation de l’utilisateur, spécifiez un nom descriptif qui identifie les utilisateurs, groupes ou objets contact auxquels le plan de numérotation sera affecté.</span><span class="sxs-lookup"><span data-stu-id="0b251-149">For user dial plans, you should specify a descriptive name that identifies the users, groups, or contact objects to which the dial plan will be assigned.</span></span> <span data-ttu-id="0b251-150">Pour les plans de numérotation de site, le champ nom est prérempli avec le nom du site et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="0b251-150">For site dial plans, the Name field is prepopulated with the site name and cannot be changed.</span></span> <span data-ttu-id="0b251-151">Dans le cas d’un plan de numérotation, le champ nom est précédé de la passerelle RTC ou du nom de domaine complet (FQDN) du pool frontal et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="0b251-151">For pool dial plans, the Name field is prepopulated with the PSTN gateway or Front End pool fully qualified domain name (FQDN) and cannot be changed.</span></span>

<span data-ttu-id="0b251-152">Le *nom simple* de plan de numérotation est prérempli avec une chaîne dérivée du nom du plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-152">The dial plan *Simple Name* is prepopulated with a string that is derived from the dial plan name.</span></span> <span data-ttu-id="0b251-153">Le champ Nom simple peut être modifié, ce qui vous permet de créer une convention d’appellation plus descriptive pour vos plans de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-153">The Simple Name field is editable, which enables you to create a more descriptive naming convention for your dial plans.</span></span> <span data-ttu-id="0b251-154">La valeur *Nom simple* ne peut pas être vide et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="0b251-154">The *Simple Name* value cannot be empty and must be unique.</span></span> <span data-ttu-id="0b251-155">Une meilleure pratique consiste à développer une convention d’appellation pour votre organisation puis d’utiliser cette convention de manière cohérente sur tous les sites et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b251-155">A best practice is to develop a naming convention for your entire organization and then use this convention consistently across all sites and users.</span></span>

</div>

<div>

## <a name="description"></a><span data-ttu-id="0b251-156">Description</span><span class="sxs-lookup"><span data-stu-id="0b251-156">Description</span></span>

<span data-ttu-id="0b251-p113">Nous vous conseillons de taper le nom commun et reconnaissable du lieu géographique auquel le plan de numérotation s’applique. Par exemple, si le nom du plan de numérotation est Londres.Contoso.com, il est recommandé d’indiquer Londres dans la zone Description.</span><span class="sxs-lookup"><span data-stu-id="0b251-p113">We recommend that you type the common, recognizable name of the geographic location to which the corresponding dial plan applies. For example, if the dial plan name is London.Contoso.com, the recommended description would be London.</span></span>

</div>

<div>

## <a name="dial-in-conferencing-region"></a><span data-ttu-id="0b251-159">Région de la conférence rendez-vous</span><span class="sxs-lookup"><span data-stu-id="0b251-159">Dial-in Conferencing Region</span></span>

<span data-ttu-id="0b251-160">Si vous déployez une conférence rendez-vous, vous devrez spécifier une région en vue d’associer les numéros d’accès de conférence rendez-vous à un plan de numérotation.</span><span class="sxs-lookup"><span data-stu-id="0b251-160">If you are deploying dial-in conferencing, you will need to specify a dial-in conferencing region to associate dial-in conferencing access numbers with a dial plan.</span></span>

</div>

<div>

## <a name="external-access-prefix"></a><span data-ttu-id="0b251-161">Préfixe d’accès externe</span><span class="sxs-lookup"><span data-stu-id="0b251-161">External Access Prefix</span></span>

<span data-ttu-id="0b251-162">Vous pouvez spécifier un préfixe d’accès externe de quatre caractères ( \# , \* et 0-9) si les utilisateurs doivent composer au moins un chiffre de début supplémentaire (par exemple, 9) pour obtenir une ligne externe.</span><span class="sxs-lookup"><span data-stu-id="0b251-162">You can specify an external access prefix of up to four characters (\#, \*, and 0-9) if users need to dial one or more additional leading digits (for example, 9) to get an external line.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0b251-163">Si vous spécifiez un préfixe d’accès externe, il n’est pas nécessaire de créer une règle de normalisation supplémentaire pour inclure le préfixe.</span><span class="sxs-lookup"><span data-stu-id="0b251-163">If you specify an external access prefix, you do not need to create an additional normalization rule to accommodate the prefix.</span></span>



</div>

</div>

</div>

<div>

## <a name="normalization-rules"></a><span data-ttu-id="0b251-164">Règles de normalisation</span><span class="sxs-lookup"><span data-stu-id="0b251-164">Normalization Rules</span></span>

<span data-ttu-id="0b251-p114">Les règles de normalisation définissent la façon dont les numéros de téléphone exprimés sous différents formats doivent être acheminés pour l’emplacement nommé. La même chaîne de numéros peut être interprétée et convertie différemment en fonction des paramètres régionaux à partir desquels elle est composée. Les règles de normalisation sont nécessaires au routage des appels car les collaborateurs d’une organisation peuvent utiliser (et utilisent) différents formats lorsqu’ils entrent des numéros de téléphone dans leurs listes de contacts.</span><span class="sxs-lookup"><span data-stu-id="0b251-p114">Normalization rules define how phone numbers expressed in various formats are to be routed for the named location. The same number string may be interpreted and translated differently, depending on the locale from which it is dialed. Normalization rules are necessary for call routing because users can, and do, use various formats when entering phone numbers in their Contacts lists.</span></span>

<span data-ttu-id="0b251-168">La normalisation des numéros de téléphone fournis par l’utilisateur offre un format cohérent qui facilite les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b251-168">Normalizing user-supplied phone numbers provides a consistent format that facilitates the following tasks:</span></span>

  - <span data-ttu-id="0b251-169">Faire correspondre un numéro composé et de l’URI SIP du destinataire concerné</span><span class="sxs-lookup"><span data-stu-id="0b251-169">Match a dialed number to the intended recipient’s SIP-URI.</span></span>

  - <span data-ttu-id="0b251-170">Appliquer des règles d’autorisation de numérotation à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0b251-170">Apply dialing authorization rules to the calling party.</span></span>

<span data-ttu-id="0b251-171">Les champs numériques suivants figurent parmi ceux que vos règles de normalisation devront peut-être prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="0b251-171">The following number fields are among those that your normalization rules may need to account for:</span></span>

  - <span data-ttu-id="0b251-172">Plan de numérotation</span><span class="sxs-lookup"><span data-stu-id="0b251-172">Dial plan</span></span>

  - <span data-ttu-id="0b251-173">Indicatif du pays</span><span class="sxs-lookup"><span data-stu-id="0b251-173">Country code</span></span>

  - <span data-ttu-id="0b251-174">Indicatif régional</span><span class="sxs-lookup"><span data-stu-id="0b251-174">Area code</span></span>

  - <span data-ttu-id="0b251-175">Longueur du poste</span><span class="sxs-lookup"><span data-stu-id="0b251-175">Length of extension</span></span>

  - <span data-ttu-id="0b251-176">Préfixe de site</span><span class="sxs-lookup"><span data-stu-id="0b251-176">Site prefix</span></span>

<div>

## <a name="creating-normalization-rules"></a><span data-ttu-id="0b251-177">Création de règles de normalisation</span><span class="sxs-lookup"><span data-stu-id="0b251-177">Creating Normalization Rules</span></span>

<span data-ttu-id="0b251-178">Les règles de normalisation utilisent des expressions régulières .NET Framework pour spécifier des modèles de correspondance numérique que le serveur utilise pour convertir des chaînes de numérotation au format E.164 dans le but d’effectuer une recherche inversée du numéro.</span><span class="sxs-lookup"><span data-stu-id="0b251-178">Normalization rules use .NET Framework regular expressions to specify numeric match patterns that the server uses to translate dial strings to E.164 format for the purpose of performing reverse number lookup.</span></span> <span data-ttu-id="0b251-179">Pour cela, vous pouvez créer des règles de normalisation dans le panneau de configuration de Lync Server en entrant les expressions manuellement ou en entrant les chiffres de départ et la longueur des chaînes de numérotation à mettre en correspondance et en laissant le panneau de configuration de Lync Server générer l’expression régulière correspondante.</span><span class="sxs-lookup"><span data-stu-id="0b251-179">You create normalization rules in the Lync Server Control Panel either by entering the expressions manually, or by entering the starting digits and the length of the dial strings to be matched and letting the Lync Server Control Panel generate the corresponding regular expression for you.</span></span> <span data-ttu-id="0b251-180">Quelle que soit la méthode choisie, lorsque vous avez terminé, vous pouvez entrer un numéro test afin de vérifier que la règle de normalisation fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="0b251-180">Either way, when you finish, you can enter a test number to verify that the normalization rule works as expected.</span></span>

<span data-ttu-id="0b251-181">Pour plus d’informations sur l’utilisation des expressions régulières du .NET Framework, consultez la rubrique expressions régulières .NET Framework [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="0b251-181">For details about using .NET Framework regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

</div>

<span id="BKMK_SampleNormalizationRules"></span>

<div>

## <a name="sample-normalization-rules"></a><span data-ttu-id="0b251-182">Exemples de règles de normalisation</span><span class="sxs-lookup"><span data-stu-id="0b251-182">Sample Normalization Rules</span></span>

<span data-ttu-id="0b251-p116">Le tableau ci-dessous illustre des exemples de règles de normalisation écrites sous la forme d’expressions régulières .NET Framework. Il s’agit uniquement d’exemples qui ne doivent pas être considérés comme une référence normative pour la création de règles de normalisation.</span><span class="sxs-lookup"><span data-stu-id="0b251-p116">The following table shows sample normalization rules that are written as .NET Framework regular expressions. The samples are examples only and are not meant to be a prescriptive reference for creating your own normalization rules.</span></span>

### <a name="table-1normalization-rules-using-net-framework-regular-expressions"></a><span data-ttu-id="0b251-185">Tableau 1. Règles de normalisation à l’aide d’expressions régulières .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0b251-185">Table 1.Normalization Rules Using .NET Framework Regular Expressions</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b251-186">Nom de la règle</span><span class="sxs-lookup"><span data-stu-id="0b251-186">Rule name</span></span></th>
<th><span data-ttu-id="0b251-187">Description</span><span class="sxs-lookup"><span data-stu-id="0b251-187">Description</span></span></th>
<th><span data-ttu-id="0b251-188">Type de numéro</span><span class="sxs-lookup"><span data-stu-id="0b251-188">Number pattern</span></span></th>
<th><span data-ttu-id="0b251-189">Conversion</span><span class="sxs-lookup"><span data-stu-id="0b251-189">Translation</span></span></th>
<th><span data-ttu-id="0b251-190">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b251-190">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b251-191">4digitExtension</span><span class="sxs-lookup"><span data-stu-id="0b251-191">4digitExtension</span></span></p></td>
<td><p><span data-ttu-id="0b251-192">Traduit les numéros de poste à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="0b251-192">Translates 4-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="0b251-193">^ (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-193">^(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-194">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0b251-194">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-195">0100 est converti en +14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-195">0100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-196">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="0b251-196">5digitExtension</span></span></p></td>
<td><p><span data-ttu-id="0b251-197">Traduit les numéros de poste à 5 chiffres</span><span class="sxs-lookup"><span data-stu-id="0b251-197">Translates 5-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="0b251-198">^ 5 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-198">^5(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-199">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0b251-199">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-200">50100 est converti en +14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-200">50100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-201">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="0b251-201">7digitcallingRedmond</span></span></p></td>
<td><p><span data-ttu-id="0b251-202">Traduit les numéros à 7 chiffres en numéros locaux Redmond</span><span class="sxs-lookup"><span data-stu-id="0b251-202">Translates 7-digit numbers to Redmond local numbers</span></span></p></td>
<td><p><span data-ttu-id="0b251-203">^ (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-203">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-204">+1425$1</span><span class="sxs-lookup"><span data-stu-id="0b251-204">+1425$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-205">5550100 est converti en +14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-205">5550100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-206">7digitcallingDallas</span><span class="sxs-lookup"><span data-stu-id="0b251-206">7digitcallingDallas</span></span></p></td>
<td><p><span data-ttu-id="0b251-207">Traduit les numéros à 7 chiffres en numéros locaux Dallas</span><span class="sxs-lookup"><span data-stu-id="0b251-207">Translates 7-digit numbers to Dallas local numbers</span></span></p></td>
<td><p><span data-ttu-id="0b251-208">^ (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-208">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-209">+1972$1</span><span class="sxs-lookup"><span data-stu-id="0b251-209">+1972$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-210">5550100 est converti en +19725550100</span><span class="sxs-lookup"><span data-stu-id="0b251-210">5550100 is translated to +19725550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-211">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="0b251-211">10digitcallingUS</span></span></p></td>
<td><p><span data-ttu-id="0b251-212">Traduit des numéros à 10 chiffres aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="0b251-212">Translates 10-digit numbers in the United States</span></span></p></td>
<td><p><span data-ttu-id="0b251-213">^ (\d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-213">^(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-214">+1$1</span><span class="sxs-lookup"><span data-stu-id="0b251-214">+1$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-215">2065550100 est converti en +12065550100</span><span class="sxs-lookup"><span data-stu-id="0b251-215">2065550100 is translated to +12065550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-216">LDCallingUS</span><span class="sxs-lookup"><span data-stu-id="0b251-216">LDCallingUS</span></span></p></td>
<td><p><span data-ttu-id="0b251-217">Traduit des numéros avec des préfixes longue distance aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="0b251-217">Translates numbers with long distance prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="0b251-218">^ 1 (\d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-218">^1(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-219">+$1</span><span class="sxs-lookup"><span data-stu-id="0b251-219">+$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-220">12145550100 est converti en +2145550100</span><span class="sxs-lookup"><span data-stu-id="0b251-220">12145550100 is translated to +2145550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-221">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="0b251-221">IntlCallingUS</span></span></p></td>
<td><p><span data-ttu-id="0b251-222">Traduit des numéros avec des préfixes internationaux aux États-Unis</span><span class="sxs-lookup"><span data-stu-id="0b251-222">Translates numbers with international prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="0b251-223">^011(\d\*)$</span><span class="sxs-lookup"><span data-stu-id="0b251-223">^011(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="0b251-224">+$1</span><span class="sxs-lookup"><span data-stu-id="0b251-224">+$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-225">01191445550100 est converti en +91445550100</span><span class="sxs-lookup"><span data-stu-id="0b251-225">01191445550100 is translated to +91445550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-226">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="0b251-226">RedmondOperator</span></span></p></td>
<td><p><span data-ttu-id="0b251-227">Traduit 0 par l’opérateur de Redmond</span><span class="sxs-lookup"><span data-stu-id="0b251-227">Translates 0 to Redmond Operator</span></span></p></td>
<td><p><span data-ttu-id="0b251-228">^0$</span><span class="sxs-lookup"><span data-stu-id="0b251-228">^0$</span></span></p></td>
<td><p><span data-ttu-id="0b251-229">+14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-229">+14255550100</span></span></p></td>
<td><p><span data-ttu-id="0b251-230">0 est converti en +14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-230">0 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-231">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-231">RedmondSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0b251-232">Traduit les numéros avec un préfixe réseau (6) et le code de site de Redmond (222)</span><span class="sxs-lookup"><span data-stu-id="0b251-232">Translates numbers with on-net prefix (6) and Redmond site code (222)</span></span></p></td>
<td><p><span data-ttu-id="0b251-233">^ 6222 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-233">^6222(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-234">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0b251-234">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-235">62220100 est converti en +14255550100</span><span class="sxs-lookup"><span data-stu-id="0b251-235">62220100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-236">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-236">NYSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0b251-237">Traduit les numéros avec un préfixe réseau (6) et le code de site New York (333)</span><span class="sxs-lookup"><span data-stu-id="0b251-237">Translates numbers with on-net prefix (6) and NY site code (333)</span></span></p></td>
<td><p><span data-ttu-id="0b251-238">^ 6333 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-238">^6333(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-239">+1202555$1</span><span class="sxs-lookup"><span data-stu-id="0b251-239">+1202555$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-240">63330100 est converti en +12025550100</span><span class="sxs-lookup"><span data-stu-id="0b251-240">63330100 is translated to +12025550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-241">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-241">DallasSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0b251-242">Traduit les numéros avec un préfixe réseau (6) et le code de site Dallas (444)</span><span class="sxs-lookup"><span data-stu-id="0b251-242">Translates numbers with on-net prefix (6) and Dallas site code (444)</span></span></p></td>
<td><p><span data-ttu-id="0b251-243">^ 6444 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0b251-243">^6444(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0b251-244">+1972555$1</span><span class="sxs-lookup"><span data-stu-id="0b251-244">+1972555$1</span></span></p></td>
<td><p><span data-ttu-id="0b251-245">64440100 est converti en +19725550100</span><span class="sxs-lookup"><span data-stu-id="0b251-245">64440100 is translated to +19725550100</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b251-246">Le tableau ci-dessous illustre un exemple de plan de numérotation pour Redmond, Washington, États-Unis, basé sur les règles de normalisation indiquées dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="0b251-246">The following table illustrates a sample dial plan for Redmond, Washington, United States, based on the normalization rules shown in the previous table.</span></span>

### <a name="table-2-redmond-dial-plan-based-on-normalization-rules-shown-in-table-1"></a><span data-ttu-id="0b251-p117">Tableau 2. Plan de numérotation pour Redmond basé sur les règles de normalisation mentionnées dans le Tableau 1</span><span class="sxs-lookup"><span data-stu-id="0b251-p117">Table 2. Redmond Dial Plan Based on Normalization Rules Shown in Table 1</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b251-249">Redmond.forestFQDN</span><span class="sxs-lookup"><span data-stu-id="0b251-249">Redmond.forestFQDN</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b251-250">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="0b251-250">5digitExtension</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-251">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="0b251-251">7digitcallingRedmond</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-252">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="0b251-252">10digitcallingUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-253">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="0b251-253">IntlCallingUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-254">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-254">RedmondSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-255">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-255">NYSitePrefix</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b251-256">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0b251-256">DallasSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b251-257">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="0b251-257">RedmondOperator</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="0b251-p118">Les noms des règles de normalisation indiqués dans le tableau précédent n'incluent pas d'espaces, mais c'est une question de choix. Le premier nom du tableau, par exemple, aurait pu s'écrire « 5 digit extension » ou « 5-digit Extension » et être toujours valide.</span><span class="sxs-lookup"><span data-stu-id="0b251-p118">The normalization rules names shown in the preceding table do not include spaces, but this is a matter of choice. The first name in the table, for example, could have been written "5 digit extension" or "5-digit Extension" and still be valid.</span></span>



<span data-ttu-id="0b251-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b251-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

