---
title: 'Lync Server 2013 : À propos des régions réseau, des sites réseau et des sous-réseaux'
description: 'Lync Server 2013 : à propos des zones, des sites et des sous-réseaux réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: About network regions, sites, and subnets
ms:assetid: 6662123a-d011-408c-a290-92b2a8589943
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398467(v=OCS.15)
ms:contentKeyID: 48184335
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3c7f660f3c72003527e0721c3f9702865e9b9b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439519"
---
# <a name="about-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="c0c0b-103">À propos des régions réseau, des sites réseau et des sous-réseaux dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0c0b-103">About network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0c0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0c0b-104">

<span> </span></span></span>

<span data-ttu-id="c0c0b-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="c0c0b-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="c0c0b-106">Les fonctionnalités avancées de voix entreprise décrites dans cette section partagent certaines exigences de configuration pour les zones réseau, les sites réseau et les sous-réseaux.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-106">The advanced Enterprise Voice features described in this section share certain configuration requirements for network regions, network sites, and subnets.</span></span> <span data-ttu-id="c0c0b-107">Par exemple, les trois fonctionnalités avancées nécessitent que chaque sous-réseau de votre topologie soit associé à un *site réseau* spécifique et chaque site réseau doit être associé à une *région réseau*.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-107">For example, all three advanced features require that each subnet in your topology be associated with a specific *network site*, and each network site must be associated with a *network region*.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c0c0b-108">Avant de commencer la configuration du réseau pour le contrôle d’admission des appels, E9-1-1 ou le contournement multimédia, assurez-vous d’avoir examiné les informations supplémentaires sur les paramètres réseau dans les <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">paramètres réseau pour les fonctionnalités avancées d’Enterprise voix dans Lync Server 2013</A> de la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-108">Before you begin network configuration for call admission control, E9-1-1, or media bypass, make sure that you reviewed additional information about network settings in the <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A> topic in the Planning documentation.</span></span> <span data-ttu-id="c0c0b-109">Pour plus d’informations sur la configuration du réseau essentiellement sur le contrôle d’admission des appels, voir <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">définir vos exigences de contrôle d’admission des appels dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-109">For details about network configuration primarily about call admission control, also see <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<span data-ttu-id="c0c0b-110">Le contrôle d’admission des appels et E9-1-1 ont des exigences de configuration supplémentaires pour les sites réseau :</span><span class="sxs-lookup"><span data-stu-id="c0c0b-110">Call admission control and E9-1-1 have additional configuration requirements for network sites:</span></span>

  - <span data-ttu-id="c0c0b-111">Le contrôle d’admission des appels nécessite de spécifier un *profil de stratégie de bande passante* pour chaque site soumis à des restrictions de bande passante de réseau étendu (WAN).</span><span class="sxs-lookup"><span data-stu-id="c0c0b-111">Call admission control requires that a *bandwidth policy profile* be specified for each site that is constrained by WAN bandwidth limitations.</span></span> <span data-ttu-id="c0c0b-112">Si vous envisagez de déployer le contrôle d’admission des appels, vous devez [créer des profils de stratégie de bande passante dans Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) avant de configurer les sites de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-112">If you plan to deploy call admission control, you must [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) before you configure your network sites.</span></span>

  - <span data-ttu-id="c0c0b-113">E9-1-1 nécessite de spécifier une *stratégie d’emplacement* pour chaque site.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-113">E9-1-1 requires that a *location policy* be specified for each site.</span></span> <span data-ttu-id="c0c0b-114">Si vous envisagez de déployer E9-1-1, vous devez [créer des stratégies d’emplacement dans Lync Server 2013](lync-server-2013-create-location-policies.md) avant de configurer les sites de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-114">If you plan to deploy E9-1-1, you must [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) before you configure your network sites.</span></span>

<div>

## <a name="create-or-modify-network-regions-network-sites-and-subnets"></a><span data-ttu-id="c0c0b-115">Créer ou modifier des régions, des sites et des sous-réseaux réseau</span><span class="sxs-lookup"><span data-stu-id="c0c0b-115">Create or Modify Network Regions, Network Sites, and Subnets</span></span>

<span data-ttu-id="c0c0b-116">Les rubriques suivantes décrivent les étapes permettant de créer ou de modifier des zones et des sites réseau, et d’associer des sous-réseaux aux sites réseau.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-116">The following topics provide steps to create or modify network regions and network sites, and to associate subnets with network sites.</span></span> <span data-ttu-id="c0c0b-117">Ces rubriques ne sont pas spécifiques à toutes les fonctionnalités avancées de voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="c0c0b-117">These topics are not specific to any particular advanced Enterprise Voice feature.</span></span>

  - [<span data-ttu-id="c0c0b-118">Créer ou modifier une région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0c0b-118">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="c0c0b-119">Création ou modification d’un site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0c0b-119">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="c0c0b-120">Association d’un sous-réseau à un site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0c0b-120">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

<span data-ttu-id="c0c0b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0c0b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

