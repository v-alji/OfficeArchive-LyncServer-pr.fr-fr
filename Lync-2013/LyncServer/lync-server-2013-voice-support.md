---
title: Prise en charge vocale dans Lync Server 2013
description: Prise en charge de la voix de Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice support
ms:assetid: d151caa8-2ee4-4bfa-be53-428570aae1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398896(v=OCS.15)
ms:contentKeyID: 48185436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b97b8e5ade1d97d458117adc04f161077abc9beb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443901"
---
# <a name="voice-support-in-lync-server-2013"></a><span data-ttu-id="6fdcb-103">Prise en charge vocale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fdcb-103">Voice support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fdcb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fdcb-104">

<span> </span></span></span>

<span data-ttu-id="6fdcb-105">_**Dernière modification de la rubrique :** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="6fdcb-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="6fdcb-106">Si votre déploiement inclut un pool frontal, vous pouvez déployer la prise en charge pour Enterprise Voice, la solution VoIP (Voice over IP) proposée par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6fdcb-106">If your deployment includes a Front End pool, you can deploy support for Enterprise Voice, the Voice over IP (VoIP) solution offered by Microsoft.</span></span> <span data-ttu-id="6fdcb-107">La voix sur IP (VoIP) est une alternative logicielle de la téléphonie classique basée sur le PBX.</span><span class="sxs-lookup"><span data-stu-id="6fdcb-107">Voice over IP (VoIP) is a software-based alternative to traditional PBX-based telephony.</span></span> <span data-ttu-id="6fdcb-108">Même si l’expérience d’appel VoIP est semblable à l’expérience de téléphonie classique, Enterprise Voice inclut des fonctionnalités qui permettent une communication et une collaboration plus riches.</span><span class="sxs-lookup"><span data-stu-id="6fdcb-108">Although the VoIP call experience is similar to the traditional telephony experience, Enterprise Voice includes features that enable richer communication and collaboration.</span></span> <span data-ttu-id="6fdcb-109">Par exemple, vous pouvez configurer le déploiement de votre voix entreprise pour permettre aux utilisateurs de Lync 2013 et de Lync Phone Edition d’afficher les informations de présence ou les informations d’emplacement améliorées pour les contacts du carnet d’adresses de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6fdcb-109">For example, your Enterprise Voice deployment can be configured to make it possible for Lync 2013 and Lync Phone Edition users to view enhanced presence information or location information for contacts in your organization’s address book.</span></span> <span data-ttu-id="6fdcb-110">Certaines fonctionnalités de Lync Server 2013 peuvent être activées par le biais de l’intégration avec d’autres charges de travail Lync Server 2013 et la messagerie unifiée Exchange (MU).</span><span class="sxs-lookup"><span data-stu-id="6fdcb-110">Some Lync Server 2013 features are enabled through integration with other Lync Server 2013 workloads and with Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="6fdcb-111">Pour plus d’informations sur les fonctionnalités et les fonctionnalités disponibles dans voix entreprise et sur la planification du déploiement, reportez-vous à la rubrique [planification d’Enterprise Voice dans Lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="6fdcb-111">For details about the features and functionality available with Enterprise Voice and how to plan for deployment, see [Planning for Enterprise Voice in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6fdcb-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6fdcb-112">In This Section</span></span>

  - [<span data-ttu-id="6fdcb-113">Prise en charge des jonctions SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fdcb-113">SIP trunking support in Lync Server 2013</span></span>](lync-server-2013-sip-trunking-support.md)

  - [<span data-ttu-id="6fdcb-114">Prise en charge des connexions SIP directes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fdcb-114">Direct SIP connections support in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections-support.md)

  - [<span data-ttu-id="6fdcb-115">Prise en charge de la messagerie unifiée Exchange dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fdcb-115">Exchange Unified Messaging (UM) support in Lync Server 2013</span></span>](lync-server-2013-exchange-unified-messaging-um-support.md)

  - [<span data-ttu-id="6fdcb-116">Prise en charge d’E9-1-1 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fdcb-116">E9-1-1 support in Lync Server 2013</span></span>](lync-server-2013-e9-1-1-support.md)

<span data-ttu-id="6fdcb-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fdcb-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

