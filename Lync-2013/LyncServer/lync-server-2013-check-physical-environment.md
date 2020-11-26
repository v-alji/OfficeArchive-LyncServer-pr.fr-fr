---
title: 'Lync Server 2013 : vérifier l’environnement physique'
description: 'Lync Server 2013 : vérifier l’environnement physique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing physical environmental checks
ms:assetid: 153aee5e-3adf-4dbf-bf41-53e4fba51fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720558(v=OCS.15)
ms:contentKeyID: 63969582
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d963485b109e0afdf21b3a9085fa28884dfc3100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434997"
---
# <a name="performing-physical-environmental-checks"></a><span data-ttu-id="15a34-103">Exécution des tests physiques sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="15a34-103">Performing physical environmental checks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15a34-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15a34-104">

<span> </span></span></span>

<span data-ttu-id="15a34-105">_**Dernière modification de la rubrique :** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="15a34-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="15a34-106">Avant de vérifier les performances, la disponibilité et les fonctionnalités du déploiement de Lync Server 2013, vous devez vérifier l’environnement physique.</span><span class="sxs-lookup"><span data-stu-id="15a34-106">Before checking the performance, availability, and functionality of the Lync Server 2013 deployment, you should check the physical environment.</span></span> <span data-ttu-id="15a34-107">Par exemple, il se peut que la température de la salle du serveur soit réduite ou qu’un câble réseau puisse être remplacé.</span><span class="sxs-lookup"><span data-stu-id="15a34-107">For example, the server room temperature might have to be lowered, or a network cable might have to be replaced.</span></span> <span data-ttu-id="15a34-108">Pour obtenir de meilleurs résultats, effectuez les inspections physiques en environnement suivantes :</span><span class="sxs-lookup"><span data-stu-id="15a34-108">For best results, perform the following physical environmental inspections:</span></span>

  - <span data-ttu-id="15a34-109">**Mesures de sécurité physiques**   Il est possible de sécuriser les protections de sécurité physiques telles que les verrouillages, les portes et les salles d’accès restreints.</span><span class="sxs-lookup"><span data-stu-id="15a34-109">**Physical security measures**   Physical security protection such as locks, doors, and restricted-access rooms must be secured.</span></span> <span data-ttu-id="15a34-110">Recherchez les entrées non autorisées et imposées et les signes d’endommagement de l’équipement.</span><span class="sxs-lookup"><span data-stu-id="15a34-110">Check for any unauthorized and forced entries and signs of equipment damage.</span></span>

  - <span data-ttu-id="15a34-111">**Température et humidité**   La surchauffe, le faible débit d’air et l’humidité peuvent entraîner une surchauffe des composants matériels.</span><span class="sxs-lookup"><span data-stu-id="15a34-111">**Temperature and humidity**   High temperature, poor air flow, and humidity can cause hardware components to overheat.</span></span> <span data-ttu-id="15a34-112">Vérifiez la température et l’humidité pour vous aider à vous assurer que les systèmes environnementaux tels que le chauffage et le conditionnement d’air peuvent respecter les conditions et fonctions acceptables dans les spécifications du fabricant du matériel.</span><span class="sxs-lookup"><span data-stu-id="15a34-112">Check temperature and humidity to help to make sure that the environmental systems such as heating and air conditioning can maintain acceptable conditions and function within the hardware manufacturer's specifications.</span></span> <span data-ttu-id="15a34-113">Lorsque de nouveaux équipements sont installés récemment, assurez-vous également que le flux d’air vers et depuis les serveurs n’est pas entravé et conforme aux spécifications du fabricant.</span><span class="sxs-lookup"><span data-stu-id="15a34-113">When new equipment has recently been installed, also check that air flow both to and from the servers is unimpeded and meets manufacturer spec.</span></span>

  - <span data-ttu-id="15a34-114">**Appareils et composants**   L’organisation Lync Server 2013 repose sur un réseau physique opérationnel et sur le matériel associé.</span><span class="sxs-lookup"><span data-stu-id="15a34-114">**Devices and components**   The Lync Server 2013 organization relies on a functioning physical network and related hardware.</span></span> <span data-ttu-id="15a34-115">Assurez-vous que les routeurs, commutateurs, concentrateurs, câbles physiques et connecteurs sont opérationnels.</span><span class="sxs-lookup"><span data-stu-id="15a34-115">Make sure that routers, switches, hubs, physical cables, and connectors are operational.</span></span>

<span data-ttu-id="15a34-116">Les spécificités de l’exécution de ces tests dépendent considérablement de votre site d’installation et du matériel de serveur choisi.</span><span class="sxs-lookup"><span data-stu-id="15a34-116">The specifics on how to perform these checks will depend greatly on your installation site and the server hardware that was chosen.</span></span> <span data-ttu-id="15a34-117">La première fois que vous effectuez cette vérification, reportez-vous à la documentation matérielle et notez les paramètres souhaités pour référence future.</span><span class="sxs-lookup"><span data-stu-id="15a34-117">The first time that you perform this check, refer to the hardware documentation and note the desired parameters for future reference.</span></span>

### <a name="desired-server-space-environment"></a><span data-ttu-id="15a34-118">Environnement d’espace serveur souhaité</span><span class="sxs-lookup"><span data-stu-id="15a34-118">Desired server space environment</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15a34-119">Paramètre</span><span class="sxs-lookup"><span data-stu-id="15a34-119">Parameter</span></span></th>
<th><span data-ttu-id="15a34-120">Valeur ou plage souhaitée</span><span class="sxs-lookup"><span data-stu-id="15a34-120">Desired value or range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15a34-121">Surchauffe</span><span class="sxs-lookup"><span data-stu-id="15a34-121">Temperature</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a34-122">Humidité ambiante</span><span class="sxs-lookup"><span data-stu-id="15a34-122">Humidity</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a34-123">Face du serveur face</span><span class="sxs-lookup"><span data-stu-id="15a34-123">Front of server faces</span></span></p></td>
<td><p><span data-ttu-id="15a34-124">Allée réactive/allée froide</span><span class="sxs-lookup"><span data-stu-id="15a34-124">Hot aisle / cold aisle</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a34-125">Dégagement de l’échappement n’est pas entravée</span><span class="sxs-lookup"><span data-stu-id="15a34-125">Unimpeded exhaust clearance</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="15a34-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15a34-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

