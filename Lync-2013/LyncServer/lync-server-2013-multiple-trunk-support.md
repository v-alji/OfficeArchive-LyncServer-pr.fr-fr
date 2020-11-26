---
title: 'Lync Server 2013 : prise en charge de plusieurs Trunks'
description: 'Lync Server 2013 : prise en charge de plusieurs ISL.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Multiple trunk support
ms:assetid: a1309c09-ad9a-4c54-9650-4e3f5b2a4a00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205127(v=OCS.15)
ms:contentKeyID: 48184948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bbabb90405b3fdae47a59ba8a0798743943216d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425200"
---
# <a name="multiple-trunk-support-in-lync-server-2013"></a><span data-ttu-id="b272e-103">Prise en charge de plusieurs Trunks dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b272e-103">Multiple trunk support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b272e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b272e-104">

<span> </span></span></span>

<span data-ttu-id="b272e-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b272e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b272e-106">La fonctionnalité Lync Server 2013 prend en charge plusieurs associations entre les passerelles et les serveurs de médiation.</span><span class="sxs-lookup"><span data-stu-id="b272e-106">Lync Server 2013 functionality supports multiple associations between gateways and Mediation Servers.</span></span> <span data-ttu-id="b272e-107">Pour ce faire, vous devez définir une ligne Trunk, qui est une association logique entre une grappe de serveurs de médiation et une passerelle de réseau téléphonique commuté (PSTN), un contrôleur de bordure de session (SBC) ou un PBX IP.</span><span class="sxs-lookup"><span data-stu-id="b272e-107">These associations are made by defining a trunk, which is a logical association between a Mediation Server pool and a public switched telephone network (PSTN) gateway, Session Border Controller (SBC), or IP-PBX.</span></span> <span data-ttu-id="b272e-108">Utilisez le générateur de topologie pour associer des passerelles aux serveurs de médiation (c’est-à-dire, des Trunks).</span><span class="sxs-lookup"><span data-stu-id="b272e-108">Use the Topology Builder to associate gateways with Mediation Servers (that is, trunks).</span></span>

  - <span data-ttu-id="b272e-109">Pour attribuer ou supprimer un Trunk dans Lync Server 2013, vous devez commencer par définir un Trunk dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="b272e-109">To assign or remove a trunk in Lync Server 2013, you must first define a trunk in Topology Builder.</span></span> <span data-ttu-id="b272e-110">Un Trunk est composé de l’Association suivante : nom de domaine complet (FQDN) du serveur de médiation, port d’écoute du serveur de médiation, nom de domaine complet de la passerelle et port d’écoute de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="b272e-110">A trunk consists of the following association: Mediation Server fully qualified domain name (FQDN), the Mediation Server listening port, the gateway FQDN, and the gateway listening port.</span></span>

  - <span data-ttu-id="b272e-111">Pour configurer plusieurs Trunks, vous pouvez créer plusieurs associations entre la même passerelle et le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="b272e-111">To configure multiple trunks, you can create multiple associations between the same gateway and the Mediation Server.</span></span> <span data-ttu-id="b272e-112">Cela fournit une résilience supplémentaire à l’infrastructure voix entreprise, qui est particulièrement utile dans les scénarios d’interopération de PBX (Private Branch Exchange).</span><span class="sxs-lookup"><span data-stu-id="b272e-112">This provides additional resiliency to the Enterprise Voice infrastructure, which is especially useful in private branch exchange (PBX) interoperational scenarios.</span></span>

<span data-ttu-id="b272e-113">Lorsqu’une jonction est définie, elle doit être associée à un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="b272e-113">When a trunk is defined, it must be associated to a route.</span></span> <span data-ttu-id="b272e-114">Pour associer un Trunk à un itinéraire, vous devez définir un nom simple pour le Trunk dans le générateur de topologie.</span><span class="sxs-lookup"><span data-stu-id="b272e-114">To associate a trunk to a route, you define a simple name for the trunk in Topology Builder.</span></span> <span data-ttu-id="b272e-115">Ce nom simple est utilisé en tant que nom du Trunk dans le panneau de configuration de Lync Server, dans lequel les lignes peuvent être associées aux itinéraires.</span><span class="sxs-lookup"><span data-stu-id="b272e-115">This simple name is used as the trunk name in the Lync Server Control Panel, where trunks can be associated with routes.</span></span> <span data-ttu-id="b272e-116">Le nom de Trunk simple est utilisé comme nom de passerelle de Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b272e-116">The simple trunk name is used as the gateway name from the Lync Server Management Shell.</span></span>

    New-CsVoiceRoute -Identity <RouteId> -NumberPattern <String> -PstnUsages @{add="<UsageString>"} -PstnGatewayList @{add="<TrunkSimpleName>"}

<span data-ttu-id="b272e-117">L’administrateur doit sélectionner une Trunk par défaut associée à un serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="b272e-117">The administrator must select a default trunk associated with a Mediation Server.</span></span> <span data-ttu-id="b272e-118">Dans le générateur de topologie, cliquez avec le bouton droit sur le serveur de médiation associé, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b272e-118">From the Topology Builder, right-click the associated Mediation Server, and then click **Properties**.</span></span> <span data-ttu-id="b272e-119">Spécifiez la passerelle par défaut du serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="b272e-119">Specify the default gateway for the Mediation Server.</span></span>

<span data-ttu-id="b272e-120">Le diagramme suivant illustre les différentes liaisons définies pour chaque serveur et passerelle de médiation.</span><span class="sxs-lookup"><span data-stu-id="b272e-120">The following diagram illustrates the multiple trunks that are defined for each Mediation Server and gateway.</span></span>

<span data-ttu-id="b272e-121">**Routage de l’interligne M-N**</span><span class="sxs-lookup"><span data-stu-id="b272e-121">**M-N Trunk Routing**</span></span>

<span data-ttu-id="b272e-122">![Affectations de plusieurs tronçons.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Affectations de plusieurs tronçons.")</span><span class="sxs-lookup"><span data-stu-id="b272e-122">![Multiple trunk assignments.](images/JJ205127.c61cd9a7-d8d9-4e02-83b9-ab62519a48c4(OCS.15).jpg "Multiple trunk assignments.")</span></span>

<span data-ttu-id="b272e-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b272e-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

