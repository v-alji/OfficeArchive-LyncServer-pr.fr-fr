---
title: Migration du serveur de médiation
description: Migration du serveur de médiation.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Mediation Server
ms:assetid: b0b77121-2c8f-413e-b276-dbf1038361d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205173(v=OCS.15)
ms:contentKeyID: 48185117
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31cc4c95f0e9c86b48594238218db22f3ec1a387
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446870"
---
# <a name="migrate-mediation-server"></a><span data-ttu-id="06780-103">Migration du serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="06780-103">Migrate Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06780-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06780-104">

<span> </span></span></span>

<span data-ttu-id="06780-105">_**Dernière modification de la rubrique :** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="06780-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="06780-106">Votre serveur de médiation est fusionné dans votre topologie pilote Lync Server 2013 lorsque vous exécutez l’Assistant Fusion.</span><span class="sxs-lookup"><span data-stu-id="06780-106">Your Mediation Server is merged into your Lync Server 2013 pilot topology when you run the Merge wizard.</span></span> <span data-ttu-id="06780-107">Toutefois, vous configurez le serveur de médiation Lync Server 2013, après la migration de tous les utilisateurs, car un pool Office Communications Server 2007 R2 ne peut pas communiquer avec un serveur de médiation Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06780-107">You configure the Lync Server 2013 Mediation Server, however, after all users are migrated because an Office Communications Server 2007 R2 pool cannot communicate with a Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="06780-108">Pendant la migration côte à côte, le pool Lync Server 2013 communique avec le serveur de médiation Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="06780-108">During the side-by-side migration, the Lync Server 2013 pool communicates with the Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="06780-109">Lorsque vous configurez votre serveur de médiation Lync Server 2013, vous devez également mettre à niveau ou remplacer vos passerelles Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="06780-109">When you configure your Lync Server 2013 Mediation Server, you must also upgrade or replace your Office Communications Server 2007 R2 gateways.</span></span> <span data-ttu-id="06780-110">Les passerelles Office Communications Server 2007 R2 ne prennent pas en charge le serveur de médiation Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06780-110">Office Communications Server 2007 R2 gateways do not support Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="06780-111">Vous devez déployer des passerelles certifiées pour Lync Server 2013 et les associer à l’aide du serveur de médiation Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06780-111">You need to deploy gateways that are certified for Lync Server 2013 and associate them with the Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="06780-112">Cette étape est nécessaire avant de pouvoir désaffecter entièrement votre déploiement d’Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="06780-112">This step is required before you can completely decommission your Office Communications Server 2007 R2 deployment.</span></span>

<span data-ttu-id="06780-113">Les rubriques de cette section décrivent les tâches de configuration que vous devez effectuer lorsque vous avez terminé la migration de Lync Server 2013 Mediation Server.</span><span class="sxs-lookup"><span data-stu-id="06780-113">The topics in this section describe configuration tasks that you need to perform after you have completed your migration of Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="06780-114">Le passage du serveur de médiation colocalisé à un serveur de médiation autonome est une tâche facultative.</span><span class="sxs-lookup"><span data-stu-id="06780-114">Transitioning the collocated Mediation Server to a stand-alone Mediation Server is an optional task.</span></span>

  - [<span data-ttu-id="06780-115">Configurer le serveur de médiation</span><span class="sxs-lookup"><span data-stu-id="06780-115">Configure Mediation Server</span></span>](configure-mediation-server.md)

  - [<span data-ttu-id="06780-116">Changer les itinéraires vocaux pour utiliser le nouveau serveur de médiation Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06780-116">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>](change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md)

  - [<span data-ttu-id="06780-117">Transition d’un serveur de médiation colocalisé vers un serveur de médiation autonome (facultatif)</span><span class="sxs-lookup"><span data-stu-id="06780-117">Transition a collocated Mediation Server to a stand-alone Mediation Server (optional)</span></span>](transition-a-collocated-mediation-server-to-a-stand-alone-mediation-server-optional.md)

<span data-ttu-id="06780-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06780-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

