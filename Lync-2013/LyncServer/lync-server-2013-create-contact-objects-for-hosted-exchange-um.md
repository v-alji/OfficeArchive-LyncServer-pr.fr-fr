---
title: 'Lync Server 2013 : Création des objets de contact pour la messagerie unifiée Exchange hébergée'
description: 'Lync Server 2013 : création d’objets de contact pour le message unifié Exchange hébergé.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431973"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="220e3-103">Création des objets de contact pour la messagerie unifiée Exchange hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="220e3-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="220e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="220e3-104">

<span> </span></span></span>

<span data-ttu-id="220e3-105">_**Dernière modification de la rubrique :** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="220e3-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="220e3-106">La procédure suivante vous explique comment créer des objets de contact de standard automatique (AA) ou d’accès d’abonné (SA) pour la messagerie unifiée Exchange hébergée.</span><span class="sxs-lookup"><span data-stu-id="220e3-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="220e3-107">Pour plus d’informations, reportez-vous à la rubrique [gestion des objets de contact Exchange hébergés dans Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="220e3-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="220e3-108">Pour plus d’informations sur la configuration des objets de contact, consultez la documentation Lync Server Management Shell pour les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="220e3-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="220e3-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="220e3-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="220e3-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="220e3-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="220e3-111">Pour que les objets de contact Lync Server 2013 puissent être activés pour la messagerie unifiée Exchange hébergée, une stratégie de messagerie vocale hébergée qui s’applique à ces derniers doit être déployée.</span><span class="sxs-lookup"><span data-stu-id="220e3-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="220e3-112">Pour plus d’informations, reportez-vous <A href="lync-server-2013-hosted-voice-mail-policies.md">à stratégies de messagerie vocale hébergées dans Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="220e3-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="220e3-113">Pour créer des objets de contact AA ou SA pour le UM Exchange hébergé</span><span class="sxs-lookup"><span data-stu-id="220e3-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="220e3-114">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="220e3-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="220e3-115">Exécutez l’applet de demande New-CsExUmContact pour créer des objets de contact requis pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="220e3-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="220e3-116">Par exemple, exécutez la commande suivante pour créer un objet de contact AA et son :</span><span class="sxs-lookup"><span data-stu-id="220e3-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="220e3-117">Ces exemples définissent les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="220e3-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="220e3-118">**SipAddress** spécifie l’adresse SIP de l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="220e3-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="220e3-119">Il doit s’agir d’une adresse qui n’a pas encore été utilisée pour configurer un objet utilisateur ou contact dans les services de domaine Active Directory (AD FS).</span><span class="sxs-lookup"><span data-stu-id="220e3-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="220e3-120">Cette valeur doit être au format "SIP : \<*SIP address*\> " comme le montre l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="220e3-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="220e3-121">**RegistrarPool** spécifie le nom de domaine complet (FQDN) du pool sur lequel le service de bureau d’enregistrement est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="220e3-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="220e3-122">Les objets de contact de MU Exchange ne peuvent pas être déplacés vers des pools qui font partie des déploiements Lync Server 2013 antérieurs à Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="220e3-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="220e3-123">**UO** spécifie l’unité d’organisation Active Directory dans laquelle se trouve l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="220e3-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="220e3-124">**DisplayNumber** spécifie le numéro de téléphone de l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="220e3-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="220e3-125">Le numéro de téléphone de chaque objet contact doit être unique.</span><span class="sxs-lookup"><span data-stu-id="220e3-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="220e3-126">Le **standard automatique indique si** l’objet contact est un standard automatique.</span><span class="sxs-lookup"><span data-stu-id="220e3-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="220e3-127">Le standard automatique propose un ensemble d’invites vocales permettant aux appelants de naviguer dans le système téléphonique et de joindre la partie qu’ils souhaitent contacter.</span><span class="sxs-lookup"><span data-stu-id="220e3-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="220e3-128">La valeur **false** (valeur par défaut) pour ce paramètre indique un objet contact d’accès abonné.</span><span class="sxs-lookup"><span data-stu-id="220e3-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="220e3-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="220e3-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

