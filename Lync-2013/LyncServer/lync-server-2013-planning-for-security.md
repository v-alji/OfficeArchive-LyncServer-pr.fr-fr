---
title: 'Lync Server 2013 : planification de la sécurité'
description: 'Lync Server 2013 : planification de la sécurité.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for security
ms:assetid: 17eeba87-cafa-4e9b-852d-c017a7d10d59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342827(v=OCS.15)
ms:contentKeyID: 56107267
ms.date: 06/22/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1abc02aa3f42a6b12c66c621b071e0b3ddb545c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424442"
---
# <a name="planning-for-security-in-lync-server-2013"></a><span data-ttu-id="90d28-103">Planification de la sécurité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-103">Planning for security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90d28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90d28-104">

<span> </span></span></span>

<span data-ttu-id="90d28-105">_**Dernière modification de la rubrique :** 2016-06-22_</span><span class="sxs-lookup"><span data-stu-id="90d28-105">_**Topic Last Modified:** 2016-06-22_</span></span>

<span data-ttu-id="90d28-106">Utilisez cette section sur la sécurité pour évaluer et gérer les risques de sécurité pour votre déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="90d28-106">Use this security section to assess and manage security risks to your deployment of Lync Server 2013.</span></span>

<span data-ttu-id="90d28-107">Même si votre déploiement de Lync Server 2013 est modeste, il est probable que les composants de votre réseau disposent de leur propre documentation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="90d28-107">Even if your Lync Server 2013 deployment is modest, you probably have components in your network that have their own security documentation.</span></span> <span data-ttu-id="90d28-108">Par conséquent, il est peu probable que cette section porte sur tous les aspects de la sécurité de tous les composants et domaines pertinents pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="90d28-108">Therefore, it is unlikely that this section covers all aspects of security for all components and areas that are pertinent to your deployment.</span></span>

<span data-ttu-id="90d28-109">Utilisez cette section comme point de départ pour gérer la sécurité de votre déploiement Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="90d28-109">Use this section as a starting point to address the security of your Lync Server 2013 deployment.</span></span> <span data-ttu-id="90d28-110">Il fournit des recommandations générales et des meilleures pratiques pour évaluer et gérer les risques les plus courants liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="90d28-110">It provides general guidelines and best practices for assessing and managing the most common security risks.</span></span> <span data-ttu-id="90d28-111">Des ressources de produit et de sécurité supplémentaires sont répertoriées à la fin de chaque rubrique.</span><span class="sxs-lookup"><span data-stu-id="90d28-111">Additional product and security resources are listed at the end of each topic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="90d28-112">La sécurité est un sujet en perpétuelle évolution.</span><span class="sxs-lookup"><span data-stu-id="90d28-112">Security is a constantly evolving topic.</span></span> <span data-ttu-id="90d28-113">À mesure que de nouvelles menaces et solutions sont susceptibles de se produire, des documents, des solutions, des méthodes et des procédures obsolètes doivent être remplacés par des contenus à jour.</span><span class="sxs-lookup"><span data-stu-id="90d28-113">As new threats and solutions arise, outdated documents, solutions, methods, and procedures should be replaced with up-to-date material.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="90d28-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="90d28-114">In This Section</span></span>

  - [<span data-ttu-id="90d28-115">Principales fonctionnalités de sécurité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-115">Key security features in Lync Server 2013</span></span>](lync-server-2013-key-security-features.md)

  - [<span data-ttu-id="90d28-116">Menaces courantes en matière de sécurité pour les jours modernes informatiques</span><span class="sxs-lookup"><span data-stu-id="90d28-116">Common security threats in modern day computing</span></span>](lync-server-2013-common-security-threats-in-modern-day-computing.md)

  - [<span data-ttu-id="90d28-117">Exclusions de l’analyse antivirus pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-117">Antivirus scanning exclusions for Lync Server 2013</span></span>](lync-server-2013-antivirus-scanning-exclusions.md)

  - [<span data-ttu-id="90d28-118">Infrastructure de sécurité pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-118">Security framework for Lync Server 2013</span></span>](lync-server-2013-security-framework-for-lync-server.md)

  - [<span data-ttu-id="90d28-119">Résoudre les problèmes de votre infrastructure de base pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-119">Addressing threats to your core infrastructure for Lync Server 2013</span></span>](lync-server-2013-addressing-threats-to-your-core-infrastructure.md)

  - [<span data-ttu-id="90d28-120">Déploiement d’un port non standard et d’un alias SQL Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d28-120">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>](deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013.md)

<span data-ttu-id="90d28-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90d28-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

