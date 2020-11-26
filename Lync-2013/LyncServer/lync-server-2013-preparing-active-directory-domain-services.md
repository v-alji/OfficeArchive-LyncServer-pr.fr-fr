---
title: 'Lync Server 2013 : Préparation des services de domaine Active Directory'
description: 'Lync Server 2013 : préparation des services de domaine Active Directory.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing Active Directory Domain Services for Lync Server 2013
ms:assetid: 7e126464-5d29-4013-9c44-0ccc2fbdea0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398630(v=OCS.15)
ms:contentKeyID: 48184620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6ecfcffd55739bc6d1bf1b83a701a0fd515ec56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424218"
---
# <a name="preparing-active-directory-domain-services-for-lync-server-2013"></a><span data-ttu-id="d3a16-103">Préparation des services de domaine Active Directory pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-103">Preparing Active Directory Domain Services for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3a16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3a16-104">

<span> </span></span></span>

<span data-ttu-id="d3a16-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d3a16-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d3a16-106">Avant de déployer et d’utiliser Lync Server 2013, vous devez préparer les services de domaine Active Directory en étendant le schéma, puis en créant et en configurant des objets.</span><span class="sxs-lookup"><span data-stu-id="d3a16-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema and then creating and configuring objects.</span></span> <span data-ttu-id="d3a16-107">Les extensions de schéma ajoutent les classes et attributs Active Directory requis par Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d3a16-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server.</span></span>

<span data-ttu-id="d3a16-108">Les rubriques de cette section expliquent comment préparer AD DS pour le déploiement de Lync Server et comment attribuer des autorisations de configuration et d’unité d’organisation.</span><span class="sxs-lookup"><span data-stu-id="d3a16-108">The topics in this section describe how to prepare AD DS for deploying Lync Server and how to assign setup and organizational unit (OU) permissions.</span></span> <span data-ttu-id="d3a16-109">Pour plus d’informations sur les changements de schéma requis pour Lync Server, voir [extensions de schéma Active Directory, classes et attributs utilisés par Lync server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="d3a16-109">For details about the schema changes required for Lync Server, see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d3a16-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d3a16-110">In This Section</span></span>

  - [<span data-ttu-id="d3a16-111">Configuration requise pour l’infrastructure Active Directory pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-111">Active Directory infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-active-directory-infrastructure-requirements.md)

  - [<span data-ttu-id="d3a16-112">Vue d’ensemble de la préparation des services de domaine Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-112">Overview of Active Directory Domain Services preparation in Lync Server 2013</span></span>](lync-server-2013-overview-of-active-directory-domain-services-preparation.md)

  - [<span data-ttu-id="d3a16-113">Préparation des services de domaine Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-113">Preparing Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="d3a16-114">Préparation des services de domaine Active Directory verrouillés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-114">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md)

  - [<span data-ttu-id="d3a16-115">Octroi d’autorisations dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3a16-115">Granting permissions in Lync Server 2013</span></span>](lync-server-2013-granting-permissions.md)

<span data-ttu-id="d3a16-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3a16-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

