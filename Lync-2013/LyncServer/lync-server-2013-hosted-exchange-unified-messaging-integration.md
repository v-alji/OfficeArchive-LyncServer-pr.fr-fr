---
title: 'Lync Server 2013 : Intégration de la messagerie unifiée Exchange hébergée'
description: 'Lync Server 2013 : intégration de la messagerie unifiée Exchange hébergée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427529"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="de7c8-103">Intégration de la messagerie unifiée Exchange hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de7c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de7c8-104">

<span> </span></span></span>

<span data-ttu-id="de7c8-105">_**Dernière modification de la rubrique :** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="de7c8-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="de7c8-106">Outre la prise en charge des versions précédentes de Lync Server 2013 pour l’intégration à des déploiements *sur site* de la messagerie unifiée Exchange, Lync Server 2013 apporte une prise en charge de l’intégration à la messagerie unifiée Exchange *hébergée* .</span><span class="sxs-lookup"><span data-stu-id="de7c8-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="de7c8-107">La messagerie unifiée Exchange hébergée permet à Lync Server 2013 de fournir la messagerie vocale à vos utilisateurs si vous les transférez en tout ou partie vers un fournisseur de services Exchange hébergé tel que Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="de7c8-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="de7c8-108">Lync Server 2013 voix entreprise utilise l’infrastructure de messagerie unifiée Exchange pour fournir les réponses aux appels, les notifications d’appel, l’accès vocal (y compris les messages vocaux) et les services de standard automatique.</span><span class="sxs-lookup"><span data-stu-id="de7c8-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="de7c8-109">Pour plus d’informations, reportez-vous à la rubrique [fonctionnalités de la messagerie unifiée intégrée et de Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="de7c8-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="de7c8-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="de7c8-110">In This Section</span></span>

  - [<span data-ttu-id="de7c8-111">Architecture et routage de la messagerie unifiée Exchange hébergée dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="de7c8-112">Stratégies de messagerie vocale hébergées dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="de7c8-113">Gestion des utilisateurs Exchange hébergés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="de7c8-114">Gestion des objets Contact Exchange hébergés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="de7c8-115">Processus de déploiement pour l’intégration de la messagerie unifiée Exchange hébergée à Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de7c8-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="de7c8-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de7c8-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

