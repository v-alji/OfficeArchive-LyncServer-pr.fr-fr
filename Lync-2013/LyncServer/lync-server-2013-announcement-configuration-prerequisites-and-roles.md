---
title: 'Lync Server 2013 : Conditions prérequises et rôles de configuration d’annonce'
description: 'Lync Server 2013 : conditions préalables et rôles de configuration d’annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439967"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="e3938-103">Conditions prérequises et rôles de configuration d’annonce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3938-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3938-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3938-104">

<span> </span></span></span>

<span data-ttu-id="e3938-105">_**Dernière modification de la rubrique :** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="e3938-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="e3938-106">Annonce est une fonction de gestion des appels voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="e3938-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="e3938-107">Cette rubrique décrit ce que vous devez mettre en place avant de pouvoir configurer l’annonce et les affectations de rôles nécessaires à l’exécution de tâches de configuration.</span><span class="sxs-lookup"><span data-stu-id="e3938-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="e3938-108">Cette section suppose que vous avez lu la documentation de planification liée à l’annonce (voir [planification des fonctionnalités de gestion des appels dans Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="e3938-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="e3938-109">Conditions préalables à la configuration de l’annonce</span><span class="sxs-lookup"><span data-stu-id="e3938-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="e3938-110">L’application d’annonce nécessite les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="e3938-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="e3938-111">service d’application</span><span class="sxs-lookup"><span data-stu-id="e3938-111">Application service</span></span>

  - <span data-ttu-id="e3938-112">application Response Group</span><span class="sxs-lookup"><span data-stu-id="e3938-112">Response Group application</span></span>

  - <span data-ttu-id="e3938-113">Magasin de fichiers, pour contenir des fichiers audio</span><span class="sxs-lookup"><span data-stu-id="e3938-113">File Store, to hold audio files</span></span>

<span data-ttu-id="e3938-114">Tous ces composants sont installés par défaut lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="e3938-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="e3938-115">Rôles de configuration d’annonce</span><span class="sxs-lookup"><span data-stu-id="e3938-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="e3938-116">Pour configurer des annonces, vous pouvez utiliser les outils d’administration suivants :</span><span class="sxs-lookup"><span data-stu-id="e3938-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="e3938-117">Panneau de configuration Lync Server</span><span class="sxs-lookup"><span data-stu-id="e3938-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="e3938-118">Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="e3938-118">Lync Server Management Shell</span></span>

<span data-ttu-id="e3938-119">La configuration de l’application d’annonce nécessite l’un des rôles d’administration suivants :</span><span class="sxs-lookup"><span data-stu-id="e3938-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="e3938-120">**CsVoiceAdministrator**   Ce rôle d’administrateur peut créer, configurer et gérer l’ensemble des stratégies et paramètres relatifs à la voix, y compris les paramètres d’annonce.</span><span class="sxs-lookup"><span data-stu-id="e3938-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="e3938-121">**CsServerAdministrator**   Ce rôle d’administrateur peut gérer, surveiller et résoudre les problèmes liés aux serveurs et services, et configurer tous les paramètres d’annonce.</span><span class="sxs-lookup"><span data-stu-id="e3938-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="e3938-122">**CsAdministrator**   Ce rôle d’administrateur peut effectuer toutes les tâches administratives et modifier tous les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e3938-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="e3938-123">**CsViewOnlyAdministrator**   Ce rôle d’administrateur peut voir le déploiement pour contrôler l’intégrité du déploiement.</span><span class="sxs-lookup"><span data-stu-id="e3938-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e3938-124">Pour plus d’informations sur les privilèges des utilisateurs d’administration, voir <A href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="e3938-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e3938-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3938-125">See Also</span></span>


[<span data-ttu-id="e3938-126">Déploiement d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3938-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="e3938-127">Planifier les fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3938-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="e3938-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3938-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

