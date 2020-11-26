---
title: 'Lync Server 2013 : connexions SIP directes'
description: 'Lync Server 2013 : connexions SIP directes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Direct SIP connections
ms:assetid: 0a37737d-9628-4e36-b27b-c134fa5a3882
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398151(v=OCS.15)
ms:contentKeyID: 48183357
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebc42cd26472bbb19c7ef886a9449ab453b90680
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429132"
---
# <a name="direct-sip-connections-in-lync-server-2013"></a><span data-ttu-id="731c5-103">Connexions SIP directes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="731c5-103">Direct SIP connections in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="731c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="731c5-104">

<span> </span></span></span>

<span data-ttu-id="731c5-105">_**Dernière modification de la rubrique :** 2012-08-13_</span><span class="sxs-lookup"><span data-stu-id="731c5-105">_**Topic Last Modified:** 2012-08-13_</span></span>

<span data-ttu-id="731c5-106">Vous pouvez utiliser des *connexions SIP directes* pour connecter le serveur Lync à l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="731c5-106">You can use *direct SIP connections* to connect Lync Server to either of the following:</span></span>

  - <span data-ttu-id="731c5-107">Un PBX IP (pour plus de détails, voir [options de déploiement SIP directes dans Lync Server 2013](lync-server-2013-direct-sip-deployment-options.md)).</span><span class="sxs-lookup"><span data-stu-id="731c5-107">An IP-PBX (for details, see [Direct SIP deployment options in Lync Server 2013](lync-server-2013-direct-sip-deployment-options.md)).</span></span>

  - <span data-ttu-id="731c5-108">Passerelle RTC (pour plus de détails, voir [options de déploiement de la passerelle RTC dans Lync Server 2013](lync-server-2013-pstn-gateway-deployment-options.md)).</span><span class="sxs-lookup"><span data-stu-id="731c5-108">A PSTN gateway (for details, see [PSTN gateway deployment options in Lync Server 2013](lync-server-2013-pstn-gateway-deployment-options.md)).</span></span>

<span data-ttu-id="731c5-109">Pour implémenter une connexion SIP directe, vous devez suivre les mêmes étapes de déploiement que dans le cadre de l’implémentation d’un Trunk SIP.</span><span class="sxs-lookup"><span data-stu-id="731c5-109">To implement a direct SIP connection, you follow essentially the same deployment steps as you would to implement a SIP trunk.</span></span> <span data-ttu-id="731c5-110">Dans les deux cas, vous implémentez la connexion à l’aide de l’interface externe d’un serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="731c5-110">In both cases, you implement the connection by using the external interface of a Mediation Server.</span></span> <span data-ttu-id="731c5-111">La seule différence réside dans le fait que vous connectez des lignes SIP à une entité externe, telle qu’une passerelle ITSP et que vous connectez des connexions SIP directes à une entité interne au sein de votre réseau local (par exemple, un PBX IP ou une passerelle RTC (réseau téléphonique commuté).</span><span class="sxs-lookup"><span data-stu-id="731c5-111">The only difference is that you connect SIP trunks to an external entity, such as an ITSP gateway, and you connect direct SIP connections to an internal entity within your local network, such as an IP-PBX or a public switched telephone network (PSTN) gateway.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="731c5-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="731c5-112">In This Section</span></span>

  - [<span data-ttu-id="731c5-113">Options de déploiement SIP direct dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="731c5-113">Direct SIP deployment options in Lync Server 2013</span></span>](lync-server-2013-direct-sip-deployment-options.md)

  - [<span data-ttu-id="731c5-114">Options de déploiement de passerelle RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="731c5-114">PSTN gateway deployment options in Lync Server 2013</span></span>](lync-server-2013-pstn-gateway-deployment-options.md)

<span data-ttu-id="731c5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="731c5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

