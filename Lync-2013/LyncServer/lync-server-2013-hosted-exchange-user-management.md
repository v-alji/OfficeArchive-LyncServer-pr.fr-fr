---
title: 'Lync Server 2013 : Gestion des utilisateurs Exchange hébergés'
description: 'Lync Server 2013 : gestion des utilisateurs Exchange hébergée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange user management
ms:assetid: e8723af5-0604-4d7d-bad2-463a9832efb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399037(v=OCS.15)
ms:contentKeyID: 48185887
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ceda9352fc627fc7b762b5995d788ffafa159ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427522"
---
# <a name="hosted-exchange-user-management-in-lync-server-2013"></a><span data-ttu-id="6196f-103">Gestion des utilisateurs Exchange hébergés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6196f-103">Hosted Exchange user management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6196f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6196f-104">

<span> </span></span></span>

<span data-ttu-id="6196f-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="6196f-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="6196f-106">Pour fournir des services de messagerie vocale aux utilisateurs de Lync Server 2013 dont les boîtes aux lettres se trouvent sur un service Exchange hébergé, vous devez activer leurs comptes d’utilisateurs pour la messagerie vocale hébergée.</span><span class="sxs-lookup"><span data-stu-id="6196f-106">To provide voice mail services for Lync Server 2013 users whose mailboxes are located on a hosted Exchange service, you must enable their user accounts for hosted voice mail.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6196f-107">Pour que l’utilisateur de 2013 la messagerie vocale hébergée puisse être activé, une stratégie de messagerie vocale hébergée qui s’applique au compte d’utilisateur correspondant doit être déployée.</span><span class="sxs-lookup"><span data-stu-id="6196f-107">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to the corresponding user account must be deployed.</span></span> <span data-ttu-id="6196f-108">La stratégie peut être globale, de site ou par utilisateur dans le champ d’application, dans la mesure où elle s’applique à l’utilisateur que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="6196f-108">The policy can be global, site, or per-user in scope, as long as it applies to the user whom you want to enable.</span></span> <span data-ttu-id="6196f-109">Pour plus d’informations, reportez-vous <A href="lync-server-2013-hosted-voice-mail-policies.md">à stratégies de messagerie vocale hébergées dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6196f-109">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="the-msexchucvoicemailsettings-attribute"></a><span data-ttu-id="6196f-110">Attribut msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="6196f-110">The msExchUCVoiceMailSettings Attribute</span></span>

<span data-ttu-id="6196f-111">Lync Server 2013 introduit un nouvel attribut utilisateur nommé **msExchUCVoiceMailSettings**, qui est créé dans le cadre de la préparation du schéma Active Directory de lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6196f-111">Lync Server 2013 introduces a new user attribute named **msExchUCVoiceMailSettings**, which is created as part of the Lync Server 2013 Active Directory schema preparation.</span></span> <span data-ttu-id="6196f-112">Cet attribut à plusieurs valeurs contient les paramètres de messagerie vocale partagés par Lync Server 2013 et le service Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="6196f-112">This multivalued attribute holds voice mail settings that are shared by Lync Server 2013 and the hosted Exchange service.</span></span>

<span data-ttu-id="6196f-113">Le service Exchange hébergé risque de définir la valeur de l’attribut msExchUCVoiceMailSettings dans le processus d’activation de la messagerie unifiée Exchange ou lors du processus de transfert de boîtes aux lettres sur un serveur Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="6196f-113">The hosted Exchange service may in some cases set the value of the msExchUCVoiceMailSettings attribute in the process of enabling Exchange UM, or during the process of transferring mailboxes to a hosted Exchange Server.</span></span> <span data-ttu-id="6196f-114">Si cet attribut n’est pas défini par Exchange, l’administrateur 2013 du serveur Lync doit le configurer en exécutant l’applet de commande Set-CsUser, comme décrit plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6196f-114">If this attribute is not set by Exchange, the Lync Server 2013 administrator must set it by running the Set-CsUser cmdlet, as described earlier in this topic.</span></span>

<span data-ttu-id="6196f-115">Les paires clé/valeur de l’attribut et leurs auteurs sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6196f-115">The attribute’s key/value pairs and their authors are shown in the following table.</span></span>

### <a name="the-msexchucvoicemailsettings-attribute-keyvalue-pairs"></a><span data-ttu-id="6196f-116">Paires clé/valeur de l’attribut msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="6196f-116">The msExchUCVoiceMailSettings Attribute Key/Value Pairs</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6196f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6196f-117">Value</span></span></th>
<th><span data-ttu-id="6196f-118">Auteur</span><span class="sxs-lookup"><span data-stu-id="6196f-118">Author</span></span></th>
<th><span data-ttu-id="6196f-119">Signification</span><span class="sxs-lookup"><span data-stu-id="6196f-119">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6196f-120">ExchangeHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="6196f-120">ExchangeHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="6196f-121">Exchange</span><span class="sxs-lookup"><span data-stu-id="6196f-121">Exchange</span></span></p></td>
<td><p><span data-ttu-id="6196f-122">L’utilisateur a été activé pour l’accès à la messagerie unifiée hébergé par Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6196f-122">User has been enabled for hosted UM access by Exchange Server.</span></span> <span data-ttu-id="6196f-123">L’application de routage de messagerie unifiée Exchange vérifie les détails de routage de la stratégie de messagerie vocale hébergée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6196f-123">The Exchange UM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6196f-124">ExchangeHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="6196f-124">ExchangeHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="6196f-125">Exchange</span><span class="sxs-lookup"><span data-stu-id="6196f-125">Exchange</span></span></p></td>
<td><p><span data-ttu-id="6196f-126">L’utilisateur a été désactivé pour l’accès à la messagerie unifiée hébergé par Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6196f-126">User has been disabled for hosted UM access by Exchange Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6196f-127">CsHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="6196f-127">CsHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="6196f-128">Lync Server</span><span class="sxs-lookup"><span data-stu-id="6196f-128">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="6196f-129">L’utilisateur a été activé pour l’accès à la messagerie unifiée hébergée par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6196f-129">User has been enabled for hosted UM access by Lync Server 2013.</span></span> <span data-ttu-id="6196f-130">L’application de routage de ExUM Lync Server 2013 vérifie la stratégie de messagerie vocale hébergée de l’utilisateur pour déterminer les détails de routage.</span><span class="sxs-lookup"><span data-stu-id="6196f-130">The Lync Server 2013 ExUM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6196f-131">CsHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="6196f-131">CsHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="6196f-132">Lync Server</span><span class="sxs-lookup"><span data-stu-id="6196f-132">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="6196f-133">L’utilisateur a été désactivé pour l’accès à la messagerie unifiée hébergée par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6196f-133">User has been disabled for hosted UM access by Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="6196f-134">Si l’attribut comporte déjà des valeurs autres que l’une des paires clé/valeur de Lync Server 2013 (CSHostedVoiceMail = 0 ou CSHostedVoiceMail = 1), un avertissement indique que l’attribut peut être géré par une autre application.</span><span class="sxs-lookup"><span data-stu-id="6196f-134">If the attribute already has values other than one of the Lync Server 2013 key/value pairs (CSHostedVoiceMail=0 or CSHostedVoiceMail=1), a warning will indicate that the attribute may be managed by a different application.</span></span> <span data-ttu-id="6196f-135">Par exemple, un avertissement s’affiche si les paires clé/valeur ExchangeHostedVoiceMail = 0 ou ExchangeHostedVoiceMail = 1 sont déjà présentes.</span><span class="sxs-lookup"><span data-stu-id="6196f-135">For example, a warning is displayed if the key/value pair ExchangeHostedVoiceMail=0 or ExchangeHostedVoiceMail=1 is already present.</span></span> <span data-ttu-id="6196f-136">Dans ce cas, vous pouvez modifier la valeur en la modifiant dans Active Directory ou en exécutant l’applet de commande suivante pour définir la valeur sur null :</span><span class="sxs-lookup"><span data-stu-id="6196f-136">In that case, you can change the value by editing it the Active Directory, or run the following cmdlet to set the value to null:</span></span><BR><span data-ttu-id="6196f-137">Set-CsUser-identité User-HostedVoicemail $null</span><span class="sxs-lookup"><span data-stu-id="6196f-137">Set-CsUser –identity user –HostedVoicemail $null</span></span>



</div>

</div>

<div>

## <a name="enabling-users-for-hosted-voice-mail"></a><span data-ttu-id="6196f-138">Activation des utilisateurs pour la messagerie vocale hébergée</span><span class="sxs-lookup"><span data-stu-id="6196f-138">Enabling Users for Hosted Voice Mail</span></span>

<span data-ttu-id="6196f-139">Pour permettre aux appels de messagerie vocale d’un utilisateur d’être routés vers la messagerie unifiée Exchange hébergée, vous devez exécuter l’applet de demande Set-CsUser pour définir la valeur du paramètre *HostedVoiceMail* .</span><span class="sxs-lookup"><span data-stu-id="6196f-139">To enable a user’s voice mail calls to be routed to hosted Exchange UM, you must run the Set-CsUser cmdlet to set the value of the *HostedVoiceMail* parameter.</span></span> <span data-ttu-id="6196f-140">Ce paramètre indique également à Lync Server 2013 d’allumer l’indicateur « appeler la messagerie vocale ».</span><span class="sxs-lookup"><span data-stu-id="6196f-140">This parameter also signals Lync Server 2013 to light up the “call voice mail” indicator.</span></span>

  - <span data-ttu-id="6196f-141">Dans l’exemple suivant, le compte d’utilisateur de Pilar Arès est activé pour la messagerie vocale hébergée :</span><span class="sxs-lookup"><span data-stu-id="6196f-141">The following example enables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $True
    
    <span data-ttu-id="6196f-142">L’applet de passe vérifie qu’une stratégie de messagerie vocale hébergée (globale, de niveau de site ou par utilisateur) s’applique à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6196f-142">The cmdlet verifies that a hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="6196f-143">S’il n’y a aucune stratégie, l’applet de passe échoue.</span><span class="sxs-lookup"><span data-stu-id="6196f-143">If no policy applies, the cmdlet fails.</span></span>

  - <span data-ttu-id="6196f-144">Dans l’exemple suivant, le compte d’utilisateur de la messagerie vocale hébergée Pilar Arès :</span><span class="sxs-lookup"><span data-stu-id="6196f-144">The following example disables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $False
    
    <span data-ttu-id="6196f-145">L’applet de passe vérifie qu’il n’y a aucune stratégie de messagerie vocale hébergée (globale, de niveau site ou par utilisateur).</span><span class="sxs-lookup"><span data-stu-id="6196f-145">The cmdlet verifies that no hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="6196f-146">Si une stratégie s’applique, l’applet de demande échoue.</span><span class="sxs-lookup"><span data-stu-id="6196f-146">If a policy does apply, the cmdlet fails.</span></span>

<span data-ttu-id="6196f-147">Pour plus d’informations sur l’utilisation de l’applet de connexion Set-CsUser, voir la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="6196f-147">For details about using the Set-CsUser cmdlet, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="6196f-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6196f-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

