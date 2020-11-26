---
title: 'Lync Server 2013 : création d’une stratégie de messagerie vocale hébergée au niveau du site'
description: 'Lync Server 2013 : création d’une stratégie de messagerie vocale hébergée au niveau du site.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site-level hosted voice mail policy
ms:assetid: 145892c8-a6ca-45fb-9e83-786f709dd775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398216(v=OCS.15)
ms:contentKeyID: 48183481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8cd578359a8d20562e8887b61b86d53332e6f8d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432113"
---
# <a name="create-a-site-level-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="b7a1e-103">Créer une stratégie de messagerie vocale hébergée au niveau du site dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7a1e-103">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7a1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7a1e-104">

<span> </span></span></span>

<span data-ttu-id="b7a1e-105">_**Dernière modification de la rubrique :** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="b7a1e-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="b7a1e-106">Une stratégie de *site* peut influer sur l’ensemble des utilisateurs hébergés sur le site pour lesquels la stratégie est définie.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-106">A *site* policy can impact all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="b7a1e-107">Si un utilisateur est configuré pour l’accès à la messagerie unifiée Exchange hébergé sans avoir reçu une stratégie par utilisateur, la stratégie de site s’applique.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-107">If a user is configured for hosted Exchange UM access and has not been assigned a Per-user policy, the site policy applies.</span></span> <span data-ttu-id="b7a1e-108">Si vous n’avez pas déployé de stratégie de site, la politique globale s’applique.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-108">If you have not deployed a site policy, the global policy applies.</span></span>

<span data-ttu-id="b7a1e-109">Pour plus d’informations sur la configuration des stratégies de site, voir la documentation Lync Server Management Shell pour les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7a1e-109">For details about configuring site policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="b7a1e-110">Nouveau-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="b7a1e-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="b7a1e-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="b7a1e-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="b7a1e-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="b7a1e-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-site-hosted-voice-mail-policy"></a><span data-ttu-id="b7a1e-113">Pour créer une stratégie de messagerie vocale hébergée sur un site</span><span class="sxs-lookup"><span data-stu-id="b7a1e-113">To create a site hosted voice mail policy</span></span>

1.  <span data-ttu-id="b7a1e-114">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="b7a1e-115">Exécutez l’applet de cmdlet New-CsHostedVoicemailPolicy pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="b7a1e-116">Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b7a1e-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity site:Redmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for the Redmond site." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="b7a1e-117">Cet exemple crée une stratégie de messagerie vocale hébergée avec l’étendue du site et définit les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7a1e-117">This example creates a hosted voice mail policy with site scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="b7a1e-118">**Identity** spécifie un identificateur unique pour la stratégie, qui inclut l’étendue.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="b7a1e-119">Dans le cas d’une stratégie avec l’étendue du site, la valeur du paramètre Identity doit être spécifiée dans le format `site:` *\<name\>* (par exemple,) `site:Redmond` .</span><span class="sxs-lookup"><span data-stu-id="b7a1e-119">For a policy with site scope, the Identity parameter value must be specified in the format `site:`*\<name\>*, for example, `site:Redmond`.</span></span>
    
      - <span data-ttu-id="b7a1e-120">**Destination** spécifie le nom de domaine complet (FQDN) du service Exchange um hébergé.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="b7a1e-121">Ce paramètre est facultatif, mais si vous tentez d’activer un utilisateur pour la messagerie vocale hébergée et que la stratégie attribuée de l’utilisateur n’a pas de valeur de destination, l’activation échoue.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="b7a1e-122">**Description** fournit des informations descriptives supplémentaires sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="b7a1e-123">**Organization** spécifie une liste séparée par des virgules des clients Exchange qui sont des utilisateurs de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="b7a1e-124">Chaque client doit être spécifié en tant que nom de domaine complet (FQDN) du client sur le service de messagerie unifiée Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="b7a1e-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

<span data-ttu-id="b7a1e-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7a1e-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

