---
title: Prise en charge d’Active Directory dans Lync Server 2013
description: Prise en charge de Lync Server 2013 Active Directory.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory support
ms:assetid: 28ed9ac4-586d-4803-ad45-99c4fa793f54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425756(v=OCS.15)
ms:contentKeyID: 48183679
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 349862b2f541ef3033c9a725a6ff04c6a4e219f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439407"
---
# <a name="active-directory-support-in-lync-server-2013"></a><span data-ttu-id="2b7b7-103">Prise en charge d’Active Directory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b7b7-103">Active Directory support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b7b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b7b7-104">

<span> </span></span></span>

<span data-ttu-id="2b7b7-105">_**Dernière modification de la rubrique :** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="2b7b7-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="2b7b7-106">Les topologies locales services de domaine Active Directory prises en charge par Lync Server 2013 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b7b7-106">The Active Directory Domain Services on-premises topologies that are supported by Lync Server 2013 are as follows:</span></span>

  - <span data-ttu-id="2b7b7-107">Forêt unique avec domaine unique</span><span class="sxs-lookup"><span data-stu-id="2b7b7-107">Single forest with single domain</span></span>

  - <span data-ttu-id="2b7b7-108">Forêt unique avec un arbre unique et plusieurs domaines</span><span class="sxs-lookup"><span data-stu-id="2b7b7-108">Single forest with a single tree and multiple domains</span></span>

  - <span data-ttu-id="2b7b7-109">Forêt unique avec plusieurs arbres et des espaces de noms disjoints</span><span class="sxs-lookup"><span data-stu-id="2b7b7-109">Single forest with multiple trees and disjoint namespaces</span></span>

  - <span data-ttu-id="2b7b7-110">Plusieurs forêts dans une topologie de forêt centrale</span><span class="sxs-lookup"><span data-stu-id="2b7b7-110">Multiple forests in a central forest topology</span></span>

  - <span data-ttu-id="2b7b7-111">Plusieurs forêts dans une topologie de forêt de ressources</span><span class="sxs-lookup"><span data-stu-id="2b7b7-111">Multiple forests in a resource forest topology</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2b7b7-112">Lync Server 2013 ne prend pas en charge les domaines à étiquette unique.</span><span class="sxs-lookup"><span data-stu-id="2b7b7-112">Lync Server 2013 does not support single-label domains.</span></span> <span data-ttu-id="2b7b7-113">Par exemple, une forêt avec un domaine racine appelé <STRONG>contoso. local</STRONG> est prise en charge, mais un domaine racine à une seule étiquette nommé <STRONG>local</STRONG> n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2b7b7-113">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a single-label root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="2b7b7-114">Pour plus d’informations, reportez-vous à l’article 300684 de la base de connaissances Microsoft, intitulé « informations sur la configuration de Windows pour les domaines avec des noms DNS en une seule étiquette » <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A> .</span><span class="sxs-lookup"><span data-stu-id="2b7b7-114">For details, see Microsoft Knowledge Base article 300684, "Information about configuring Windows for domains with single-label DNS names," at <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A>.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="2b7b7-115">Lync Server 2013 ne prend pas en charge le changement de nom de domaines.</span><span class="sxs-lookup"><span data-stu-id="2b7b7-115">Lync Server 2013 does not support renaming domains.</span></span> <span data-ttu-id="2b7b7-116">Si vous avez besoin de renommer un domaine sur lequel Lync Server est déployé, vous devez commencer par désinstaller Lync Server, puis renommer le domaine, puis réinstaller Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2b7b7-116">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

<span data-ttu-id="2b7b7-117">Pour plus d’informations sur les topologies prises en charge et la configuration requise pour les déploiements sur site, voir [Configuration requise pour les services de domaine Active Directory, support et topologies dans Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="2b7b7-117">For details about supported topologies and requirements for on-premises deployments, see [Active Directory Domain Services requirements, support, and topologies in Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) in the Planning documentation.</span></span>

<span data-ttu-id="2b7b7-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b7b7-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

