---
title: 'Lync Server 2013 : planification de la connectivité PSTN'
description: 'Lync Server 2013 : planification de la connectivité PSTN.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for PSTN connectivity
ms:assetid: 280f684a-740a-443d-8ecf-574241382a42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425749(v=OCS.15)
ms:contentKeyID: 48183684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c0df6aa6dc9d9cc8522223056f1834849e6ddb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424435"
---
# <a name="planning-for-pstn-connectivity-in-lync-server-2013"></a><span data-ttu-id="a69e0-103">Planification de la connectivité PSTN dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-103">Planning for PSTN connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a69e0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a69e0-104">

<span> </span></span></span>

<span data-ttu-id="a69e0-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a69e0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a69e0-106">Une solution VoIP à l’échelle de l’entreprise doit de toute évidence assurer l’acheminement des appels depuis et vers le réseau téléphonique commuté (RTC) avec une qualité de service constante.</span><span class="sxs-lookup"><span data-stu-id="a69e0-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="a69e0-107">Les utilisateurs qui passent et reçoivent des appels ne doivent pas être informés de la technologie sous-jacente : du point de vue de l’utilisateur, un appel entre l’infrastructure voix entreprise et le RTC devrait paraître un appel téléphonique.</span><span class="sxs-lookup"><span data-stu-id="a69e0-107">Users who place and receive calls should not be aware of the underlying technology: from the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another phone call.</span></span>

<span data-ttu-id="a69e0-108">Lync Server 2013 fournit une connectivité PSTN fiable et évolutive en utilisant les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a69e0-108">Lync Server 2013 provides reliable, scalable PSTN connectivity by using the following options:</span></span>

  - <span data-ttu-id="a69e0-109">Les **jonctions SIP** vers un fournisseur de services de téléphonie Internet (ITSP)</span><span class="sxs-lookup"><span data-stu-id="a69e0-109">**SIP trunks** to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="a69e0-110">Les **connexions SIP directes** à une passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="a69e0-110">**Direct SIP connections** to a PSTN gateway</span></span>

  - <span data-ttu-id="a69e0-111">Les **connexions SIP directes** à un système PBX</span><span class="sxs-lookup"><span data-stu-id="a69e0-111">**Direct SIP connections** to a PBX</span></span>

<span data-ttu-id="a69e0-112">Selon la taille, la couverture géographique et l’infrastructure vocale existante, une entreprise peut utiliser une ou deux des options, voire les trois, à divers emplacements.</span><span class="sxs-lookup"><span data-stu-id="a69e0-112">Depending on its size, geographic coverage, and existing voice infrastructure, an enterprise may use one, two, or even all three of these options at various locations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a69e0-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a69e0-113">In This Section</span></span>

  - [<span data-ttu-id="a69e0-114">Trunking SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-114">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)

  - [<span data-ttu-id="a69e0-115">Connexions SIP directes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-115">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)

  - [<span data-ttu-id="a69e0-116">M :N Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-116">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="a69e0-117">Règles de traduction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-117">Translation rules in Lync Server 2013</span></span>](lync-server-2013-translation-rules.md)

  - [<span data-ttu-id="a69e0-118">Planification du routage des communications vocales sortantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a69e0-118">Planning outbound voice routing in Lync Server 2013</span></span>](lync-server-2013-planning-outbound-voice-routing.md)

<span data-ttu-id="a69e0-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a69e0-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

