---
title: Options de jumelage et meilleures pratiques de Lync Server 2013 prises en charge
description: Options de jumelage et meilleures pratiques de Lync Server 2013 prises en charge.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441416"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a><span data-ttu-id="d056b-103">Options de jumelage de pool prises en charge et meilleures pratiques pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d056b-103">Supported pool pairing options and best practices for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d056b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d056b-104">

<span> </span></span></span>

<span data-ttu-id="d056b-105">_**Dernière modification de la rubrique :** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="d056b-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="d056b-106">Il n’existe aucune restriction sur la distance entre deux centres de données qui doivent inclure des listes frontales couplées.</span><span class="sxs-lookup"><span data-stu-id="d056b-106">There is no restriction on the distance between two data centers that are to include Front End pools paired with each other.</span></span> <span data-ttu-id="d056b-107">Nous vous recommandons d’utiliser deux centres de données au sein d’une même région dans le monde, grâce à des liens haut débit.</span><span class="sxs-lookup"><span data-stu-id="d056b-107">We recommend that you use two data centers in the same world region, with high-speed links between them.</span></span> <span data-ttu-id="d056b-108">Il est préférable que les deux centres de données soient suffisamment séparés pour éviter une catastrophe unique, en même temps.</span><span class="sxs-lookup"><span data-stu-id="d056b-108">It is best if the two data centers are separated enough to avoid a single disaster hitting both at the same time.</span></span>

<span data-ttu-id="d056b-109">Il est possible d’avoir deux centres de données dans les différentes régions du monde, mais peut entraîner une plus grande perte de données en raison d’une latence dans la réplication des données.</span><span class="sxs-lookup"><span data-stu-id="d056b-109">Having two data centers across world regions is possible, but could incur higher data loss due to latency in data replication.</span></span>

<span data-ttu-id="d056b-110">Quand vous préparez le jumelage des pools, gardez à l’esprit que seuls les jumelages suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="d056b-110">When you plan which pools to pair, you must keep in mind that only the following pairings are supported:</span></span>

  - <span data-ttu-id="d056b-111">Les pools Enterprise Edition peuvent uniquement être jumelés avec d’autres pools Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="d056b-111">Enterprise Edition pools can be paired only with other Enterprise Edition pools.</span></span> <span data-ttu-id="d056b-112">De même, les pools Standard Edition peuvent uniquement être jumelés avec d’autres pools Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d056b-112">Similarly, Standard Edition pools can be paired only with other Standard Edition pools.</span></span>

  - <span data-ttu-id="d056b-113">Les pools physiques peuvent uniquement être jumelés avec d’autres pools physiques.</span><span class="sxs-lookup"><span data-stu-id="d056b-113">Physical pools can be paired only with other physical pools.</span></span> <span data-ttu-id="d056b-114">De même, les pools virtuels peuvent uniquement être jumelés avec d’autres pools virtuels.</span><span class="sxs-lookup"><span data-stu-id="d056b-114">Similarly, virtual pools can be paired only with other virtual pools.</span></span>

  - <span data-ttu-id="d056b-115">Les pools associés doivent exécuter le même système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d056b-115">Pools that are paired together must be running the same operating system.</span></span>

<span data-ttu-id="d056b-p104">Ni le générateur de topologie, ni la validation des topologies n’empêcheront le jumelage de deux pools qui ne suit pas ces recommandations. Par exemple, le générateur de topologie vous permet de jumeler un pool Enterprise Edition avec un pool Standard Edition. Cependant, ces types de jumelages ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d056b-p104">Neither Topology Builder nor topology validation will prohibit pairing two pools in a way that does not follow these recommendations. For example, Topology Builder allows you to pair an Enterprise Edition pool with a Standard Edition pool. However, these types of pairings are not supported.</span></span>

<span data-ttu-id="d056b-119">Chaque pool d’une paire doit avoir la capacité de desservir tous les utilisateurs des deux pools en cas de sinistre.</span><span class="sxs-lookup"><span data-stu-id="d056b-119">Each pool in a pair should have the capacity to serve all users from both pools in the event of a disaster.</span></span>

<span data-ttu-id="d056b-120">Si vous jumelez les pools Enterprise Edition, vous pouvez également implémenter une haute disponibilité sur les serveurs dorsaux, mais pour les paires de pools Standard Edition, seules les mesures de reprise après sinistre sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="d056b-120">If you pair Enterprise Edition pools, you can also implement high availability on the Back End Servers, but for pairs of Standard Edition pools only the disaster recovery measures are available.</span></span>

<span data-ttu-id="d056b-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d056b-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

