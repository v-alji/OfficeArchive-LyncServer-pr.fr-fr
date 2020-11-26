---
title: 'Lync Server 2013 : Configuration des jonctions'
description: 'Lync Server 2013 : configuration de Trunks.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring trunks
ms:assetid: 0c339511-a185-484e-94f0-dbe918b7e48a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398170(v=OCS.15)
ms:contentKeyID: 48183389
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07d9503cd38419a7145796a6edf8484a14cdeb53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432463"
---
# <a name="configuring-trunks-in-lync-server-2013"></a><span data-ttu-id="ae054-103">Configuration des jonctions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-103">Configuring trunks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae054-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae054-104">

<span> </span></span></span>

<span data-ttu-id="ae054-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ae054-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ae054-106">Dans le cadre d’un déploiement voix entreprise, vous pouvez configurer un Trunk entre un serveur de médiation et un ou plusieurs des homologues suivants pour fournir une connectivité PSTN (réseau téléphonique commuté) pour les clients et périphériques vocaux d’entreprise au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="ae054-106">As part of Enterprise Voice deployment, you can configure a trunk between a Mediation Server and one or more of the following peers to provide public switched telephone network (PSTN) connectivity for Enterprise Voice clients and devices in your organization:</span></span>

  - <span data-ttu-id="ae054-107">Connexion de jonction SIP vers un fournisseur de services de téléphonie Internet</span><span class="sxs-lookup"><span data-stu-id="ae054-107">SIP trunk connection to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="ae054-108">Passerelle RTC</span><span class="sxs-lookup"><span data-stu-id="ae054-108">PSTN gateway</span></span>

  - <span data-ttu-id="ae054-109">Autocommutateur privé (PBX)</span><span class="sxs-lookup"><span data-stu-id="ae054-109">Private branch exchange (PBX)</span></span>

<span data-ttu-id="ae054-110">Pour plus d’informations, reportez-vous à [planification de la connectivité PSTN dans Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="ae054-110">For details, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) in the Planning documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ae054-111">Avant de commencer la configuration de Trunk, vérifiez que la topologie a été créée et que le serveur de médiation et son homologue ont été configurés et associés entre eux.</span><span class="sxs-lookup"><span data-stu-id="ae054-111">Before you begin trunk configuration, verify that the topology has been created and that the Mediation Server and its peer have been configured and associated with one another.</span></span> <span data-ttu-id="ae054-112">Pour plus d’informations, reportez-vous à la section <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">définir une passerelle dans le générateur de topologie de Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ae054-112">For details, see <A href="lync-server-2013-define-a-gateway-in-topology-builder.md">Define a gateway in Topology Builder in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="ae054-113">Dans le cadre de la configuration de Trunk, vous pouvez activer la fonctionnalité de contournement de média Lync Server 2013, qui permet aux éléments multimédias d’ignorer le serveur de médiation.</span><span class="sxs-lookup"><span data-stu-id="ae054-113">As a part of trunk configuration, you can enable the Lync Server 2013 media bypass feature, which enables media to bypass the Mediation Server.</span></span> <span data-ttu-id="ae054-114">Les Trunks peuvent être configurés avec ou sans Bypass multimédia activé, mais nous vous recommandons vivement de l’activer.</span><span class="sxs-lookup"><span data-stu-id="ae054-114">Trunks can be configured either with or without media bypass enabled, but we strongly recommend that you enable it.</span></span> <span data-ttu-id="ae054-115">Pour plus d’informations, reportez-vous à la section <A href="lync-server-2013-planning-for-media-bypass.md">planification de la dérivation multimédia dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="ae054-115">For details, see <A href="lync-server-2013-planning-for-media-bypass.md">Planning for media bypass in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ae054-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ae054-116">In This Section</span></span>

  - [<span data-ttu-id="ae054-117">Prise en charge de plusieurs Trunks dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-117">Multiple trunk support in Lync Server 2013</span></span>](lync-server-2013-multiple-trunk-support.md)

  - [<span data-ttu-id="ae054-118">Routage inter-Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-118">Inter-trunk routing in Lync Server 2013</span></span>](lync-server-2013-inter-trunk-routing.md)

  - [<span data-ttu-id="ae054-119">Afficher les informations de configuration de Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-119">View trunk configuration information in Lync Server 2013</span></span>](lync-server-2013-view-trunk-configuration-information.md)

  - [<span data-ttu-id="ae054-120">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-120">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)

  - [<span data-ttu-id="ae054-121">Configurer un Trunk sans dérivation multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-121">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)

  - [<span data-ttu-id="ae054-122">Créer une collection de paramètres de configuration de Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-122">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-a-new-collection-of-trunk-configuration-settings.md)

  - [<span data-ttu-id="ae054-123">Supprimer une collection existante de paramètres de configuration de Trunk SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-123">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="ae054-124">Modifier les paramètres de configuration de Trunk SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-124">Modify SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-modify-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="ae054-125">Tester les paramètres de configuration du Trunk SIP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-125">Test SIP trunk configuration settings in Lync Server 2013</span></span>](lync-server-2013-test-sip-trunk-configuration-settings.md)

  - [<span data-ttu-id="ae054-126">Afficher des informations sur les lignes SIP individuelles dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-126">View information about individual SIP trunks in Lync Server 2013</span></span>](lync-server-2013-view-information-about-individual-sip-trunks.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ae054-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae054-127">See Also</span></span>


[<span data-ttu-id="ae054-128">Définir une passerelle dans le générateur de topologies de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-128">Define a gateway in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-define-a-gateway-in-topology-builder.md)  


[<span data-ttu-id="ae054-129">Planification de la connectivité PSTN dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-129">Planning for PSTN connectivity in Lync Server 2013</span></span>](lync-server-2013-planning-for-pstn-connectivity.md)  
[<span data-ttu-id="ae054-130">Planification de la déviation du trafic multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae054-130">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="ae054-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae054-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

