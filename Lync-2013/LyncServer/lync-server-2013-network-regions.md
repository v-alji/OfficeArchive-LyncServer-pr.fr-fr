---
title: 'Lync Server 2013 : régions réseau'
description: 'Lync Server 2013 : régions réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425158"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="eb296-103">Régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb296-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb296-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb296-104">

<span> </span></span></span>

<span data-ttu-id="eb296-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="eb296-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="eb296-106">Les *régions réseau* sont les concentrateurs réseau ou les dorsales utilisés dans la configuration de contrôle d’admission des appels, de E9-1-1 et de contournement de média.</span><span class="sxs-lookup"><span data-stu-id="eb296-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="eb296-107">Utilisez les procédures suivantes pour afficher, créer ou modifier des régions réseau.</span><span class="sxs-lookup"><span data-stu-id="eb296-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="eb296-108">Par exemple, si vous avez déjà créé des régions réseau pour une seule fonctionnalité vocale, vous n’avez pas besoin de créer de nouvelles régions réseau. d’autres fonctionnalités avancées de voix entreprise utiliseront les mêmes régions réseau.</span><span class="sxs-lookup"><span data-stu-id="eb296-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="eb296-109">Toutefois, il est possible que vous soyez obligé de modifier la définition d’une région réseau existante pour appliquer des paramètres spécifiques à une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eb296-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="eb296-110">Par exemple, si vous avez créé des régions réseau pour le service E9-1-1 (régions n’exigeant aucun site central associé), puis que vous déployez le contrôle d’admission des appels, vous devez modifier les définitions des régions réseau afin de spécifier un site central.</span><span class="sxs-lookup"><span data-stu-id="eb296-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="eb296-111">Pour plus d’informations, voir [configurer des régions réseau pour CAC dans Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="eb296-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="eb296-112">Les exigences spécifiques aux fonctionnalités relatives aux définitions de zones réseau sont décrites dans les rubriques de déploiement de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="eb296-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="eb296-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="eb296-113">In This Section</span></span>

  - [<span data-ttu-id="eb296-114">Affichage des informations de région réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb296-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="eb296-115">Création ou modification des régions réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb296-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="eb296-116">Supprimer des zones réseau existantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb296-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="eb296-117">Référence</span><span class="sxs-lookup"><span data-stu-id="eb296-117">Reference</span></span>

[<span data-ttu-id="eb296-118">Déploiement de fonctionnalités avancées d’entreprise voix dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb296-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="eb296-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb296-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

