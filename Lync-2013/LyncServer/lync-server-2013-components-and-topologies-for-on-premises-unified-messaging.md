---
title: 'Lync Server 2013 : Composants et topologies de la messagerie unifiée locale'
description: 'Lync Server 2013 : composants et topologies pour la messagerie unifiée locale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for on-premises Unified Messaging
ms:assetid: 22fc87cf-a7e5-4c8c-bb9b-101e5380cdcf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425711(v=OCS.15)
ms:contentKeyID: 48183619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8fe2ca16ec9fbd39e9245fd366e1f7046dd16d42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394224"
---
# <a name="components-and-topologies-for-on-premises-unified-messaging-in-lync-server-2013"></a><span data-ttu-id="b3cc3-103">Composants et topologies de la messagerie unifiée locale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3cc3-103">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3cc3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3cc3-104">

<span> </span></span></span>

<span data-ttu-id="b3cc3-105">_**Dernière modification de la rubrique :** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="b3cc3-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="b3cc3-106">Cette rubrique décrit les composants Microsoft Exchange Server 2013 requis pour fournir des fonctionnalités de messagerie unifiée Exchange pour le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-106">This topic describes the Microsoft Exchange Server 2013 components required to provide Exchange Unified Messaging (UM) features to Lync Server 2013 deployment.</span></span> <span data-ttu-id="b3cc3-107">Il décrit également les topologies prises en charge pour l’intégration à la messagerie unifiée Exchange locale.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-107">It also describes the supported topologies for on-premises Exchange UM integration.</span></span>

<div>

## <a name="exchange-server-components"></a><span data-ttu-id="b3cc3-108">Composants d’Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b3cc3-108">Exchange Server Components</span></span>

<span data-ttu-id="b3cc3-109">Pour fournir les services et fonctionnalités de messagerie UNIFIÉe Exchange décrits dans les [fonctionnalités de messagerie unifiée et de Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md) aux utilisateurs voix entreprise dans votre organisation, vous devez déployer un serveur de boîte aux lettres Microsoft Exchange et un serveur d’accès au client, qui héberge les boîtes aux lettres des utilisateurs et fournit un emplacement de stockage unique pour la messagerie électronique et la messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-109">To provide the Exchange UM features and services described in [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md) to Enterprise Voice users in your organization, you must deploy an Microsoft Exchange Mailbox server and Client Access server, which hosts user mailboxes and provides a single storage location for email and voice mail.</span></span> <span data-ttu-id="b3cc3-110">La messagerie unifiée Exchange s’exécute en tant que service sur les serveurs de boîtes aux lettres Exchange et d’accès client.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-110">Exchange UM runs as a service on Exchange Mailbox and Client Access servers.</span></span>

<span data-ttu-id="b3cc3-111">Pour plus d’informations sur les composants de messagerie unifiée Exchange dans Microsoft Exchange Server 2007 et Microsoft Exchange Server 2010, voir [déploiement de la messagerie unifiée Exchange locale pour fournir la messagerie vocale Lync Server 2013](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-111">For details about Exchange UM components in Microsoft Exchange Server 2007 and Microsoft Exchange Server 2010, see [Deploying on-premises Exchange UM to provide Lync Server 2013 voice mail](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="b3cc3-112">Topologies prises en charge</span><span class="sxs-lookup"><span data-stu-id="b3cc3-112">Supported Topologies</span></span>

<span data-ttu-id="b3cc3-113">Vous pouvez déployer Lync Server 2013 et Exchange Unified Messaging (UM) dans la même forêt ou plusieurs forêts.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-113">You can deploy Lync Server 2013 and Exchange Unified Messaging (UM) in the same forest or multiple forests.</span></span> <span data-ttu-id="b3cc3-114">Si le déploiement s’étend sur plusieurs forêts, vous devez effectuer les étapes d’intégration Exchange pour chaque forêt Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-114">If the deployment spans multiple forests, you must perform the Exchange integration steps for each Exchange UM forest.</span></span> <span data-ttu-id="b3cc3-115">Par ailleurs, vous devez configurer chaque forêt Microsoft Exchange pour faire confiance aux forêts Lync Server 2013 et à la forêt Lync Server 2013 pour approuver chaque forêt Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-115">Furthermore, you must configure each Microsoft Exchange forest to trust the Lync Server 2013 forest and the Lync Server 2013 forest to trust each Exchange UM forest.</span></span> <span data-ttu-id="b3cc3-116">Outre cette approbation de forêt, les paramètres de messagerie unifiée Exchange pour tous les utilisateurs doivent être définis sur les objets utilisateur dans la forêt 2013 du serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-116">In addition to this forest trust, the Exchange UM settings for all users must be set on the user objects in the Lync Server 2013 forest.</span></span>

<span data-ttu-id="b3cc3-117">Lync Server 2013 prend en charge les topologies suivantes pour l’intégration à la messagerie unifiée Exchange :</span><span class="sxs-lookup"><span data-stu-id="b3cc3-117">Lync Server 2013 supports the following topologies for Exchange UM integration:</span></span>

  - <span data-ttu-id="b3cc3-118">Forêt unique</span><span class="sxs-lookup"><span data-stu-id="b3cc3-118">Single forest</span></span>

  - <span data-ttu-id="b3cc3-119">Domaine unique (à savoir, une seule forêt associée à un seul domaine).</span><span class="sxs-lookup"><span data-stu-id="b3cc3-119">Single domain (that is, a single forest with a single domain).</span></span> <span data-ttu-id="b3cc3-120">Lync Server 2013, Microsoft Exchange et les utilisateurs se trouvent tous dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-120">Lync Server 2013, Microsoft Exchange, and users all reside in the same domain.</span></span>

  - <span data-ttu-id="b3cc3-121">Plusieurs domaines (à savoir, un domaine racine comportant un ou plusieurs domaines enfants).</span><span class="sxs-lookup"><span data-stu-id="b3cc3-121">Multiple domain (that is, a root domain with one or more child domains).</span></span> <span data-ttu-id="b3cc3-122">Les serveurs Lync Server 2013 et Microsoft Exchange sont déployés dans différents domaines à partir du domaine dans lequel vous créez des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-122">Lync Server 2013, and Microsoft Exchange servers are deployed in different domains from the domain where you create users.</span></span> <span data-ttu-id="b3cc3-123">Les serveurs de messagerie unifiée Exchange peuvent être déployés dans différents domaines à partir du pool Lync Server 2013 pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-123">Exchange UM servers can be deployed in different domains from the Lync Server 2013 pool they support.</span></span>

  - <span data-ttu-id="b3cc3-124">Forêts multiples (c’est-à-dire, forêt de ressources).</span><span class="sxs-lookup"><span data-stu-id="b3cc3-124">Multiple forest (that is, resource forest).</span></span> <span data-ttu-id="b3cc3-125">Lync Server 2013 est déployé dans une seule forêt, et les utilisateurs sont répartis entre plusieurs forêts.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-125">Lync Server 2013 is deployed in a single forest, and then users are distributed across multiple forests.</span></span> <span data-ttu-id="b3cc3-126">Les attributs d’Exchange UM des utilisateurs doivent être répliqués dans la forêt Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-126">The users’ Exchange UM attributes must be replicated over to the Lync Server 2013 forest.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b3cc3-127">Exchange peut être déployé dans plusieurs forêts.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-127">Exchange can be deployed in multiple forests.</span></span> <span data-ttu-id="b3cc3-128">Chaque organisation Exchange peut fournir la messagerie unifiée Exchange à ses utilisateurs, ou la messagerie unifiée Exchange peut être déployée dans la même forêt que Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b3cc3-128">Each Exchange organization can provide Exchange UM to its users, or Exchange UM can be deployed in the same forest as Lync Server 2013.</span></span>

    
    <span data-ttu-id="b3cc3-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3cc3-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

