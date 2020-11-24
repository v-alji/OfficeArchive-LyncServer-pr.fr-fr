---
title: 'Lync Server 2013 : Attributs, classes et extensions deq schémas Active Directory utilisés par Lync Server'
description: 'Lync Server 2013 : extensions de schéma Active Directory, classes et attributs utilisés par Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory schema extensions, classes, and attributes used by Lync Server 2013
ms:assetid: 579bfa5a-9443-46dd-9a8e-07d00ba2824d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398379(v=OCS.15)
ms:contentKeyID: 48184188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: beac778d3315573f4d5cc6cb9c827a3a2fce9d0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393869"
---
# <a name="active-directory-schema-extensions-classes-and-attributes-used-by-lync-server-2013"></a><span data-ttu-id="e2af3-103">Attributs, classes et extensions des schémas Active Directory utilisés par Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-103">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2af3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2af3-104">

<span> </span></span></span>

<span data-ttu-id="e2af3-105">_**Dernière modification de la rubrique :** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="e2af3-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="e2af3-106">Cette section de référence contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2af3-106">This reference section includes the following information:</span></span>

  - <span data-ttu-id="e2af3-107">Extensions de schéma Active Directory nouvelles ou modifiées pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-107">Active Directory schema extensions that are new or changed for Lync Server 2013</span></span>
    
    <span data-ttu-id="e2af3-108">Le schéma Active Directory contient des définitions formels de toutes les classes d’objets qui peuvent être créées dans une forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e2af3-108">The Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="e2af3-109">Le schéma contient également des définitions formels de chaque attribut qui peut exister sur un objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e2af3-109">The schema also contains formal definitions of every attribute that can exist on an Active Directory object.</span></span> <span data-ttu-id="e2af3-110">Le catalogue global Active Directory contient des réplicas de tous les objets pour la forêt, ainsi qu’un sous-ensemble des attributs de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="e2af3-110">The Active Directory global catalog contains replicas of all the objects for the forest, along with a subset of the attributes for each object.</span></span> <span data-ttu-id="e2af3-111">Cette section décrit les classes et attributs qui sont nouveaux ou modifiés dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2af3-111">This section describes the classes and attributes that are new or changed in Lync Server 2013.</span></span>

  - <span data-ttu-id="e2af3-112">Toutes les classes utilisées par Lync Server, avec une description de chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="e2af3-112">All the classes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="e2af3-113">Tous les attributs utilisés par Lync Server, avec une description de chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="e2af3-113">All the attributes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="e2af3-114">Une liste des classes utilisées par Lync Server, ainsi que les attributs qu’ils contiennent</span><span class="sxs-lookup"><span data-stu-id="e2af3-114">A list of the classes used by Lync Server, with the attributes each may contain</span></span>

  - <span data-ttu-id="e2af3-115">Paramètres globaux et objets, en plus du service universel et des groupes d’administration créés lors de la préparation de la forêt</span><span class="sxs-lookup"><span data-stu-id="e2af3-115">Global settings and objects, in addition to the universal service and administration groups that are created during forest preparation</span></span>

  - <span data-ttu-id="e2af3-116">Entrées de contrôle d’accès (ACE) créées sur la racine de domaine et les conteneurs intégrés lors de la préparation du domaine</span><span class="sxs-lookup"><span data-stu-id="e2af3-116">Access control entries (ACEs) that are created on the domain root and built-in containers during domain preparation</span></span>

  - <span data-ttu-id="e2af3-117">Modifications effectuées sur une unité d’organisation Active Directory par l’applet de contrôle Grant \_ CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="e2af3-117">Changes that are made on an Active Directory organizational unit (OU) by the Grant\_CsSetupPermission cmdlet.</span></span>

  - <span data-ttu-id="e2af3-118">Les modifications apportées sur une unité d’organisation Active Directory par l’applet de contrôle Grant \_ CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="e2af3-118">Changes that are made on an Active Directory OU by the Grant\_CsOUPermission cmdlet.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e2af3-119">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e2af3-119">In This Section</span></span>

  - [<span data-ttu-id="e2af3-120">Modifications de schéma dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-120">Schema changes in Lync Server 2013</span></span>](lync-server-2013-schema-changes-in-lync-server-2013.md)

  - [<span data-ttu-id="e2af3-121">Descriptions et classes de schéma dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-121">Schema classes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-classes-and-descriptions.md)

  - [<span data-ttu-id="e2af3-122">Attributs et descriptions de schéma dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-122">Schema attributes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-and-descriptions.md)

  - [<span data-ttu-id="e2af3-123">Attributs de schéma par classe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-123">Schema attributes by class in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-by-class.md)

  - [<span data-ttu-id="e2af3-124">Modifications apportées par la préparation de la forêt dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-124">Changes made by forest preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-forest-preparation.md)

  - [<span data-ttu-id="e2af3-125">Modifications apportées par la préparation du domaine dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-125">Changes made by domain preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-domain-preparation.md)

  - [<span data-ttu-id="e2af3-126">Modifications apportées par Grant-CsSetupPermission dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-126">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission)

  - [<span data-ttu-id="e2af3-127">Modifications apportées par Grant-CsOUPermission dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2af3-127">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission)

<span data-ttu-id="e2af3-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2af3-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

