---
title: Conditions préalables et droits d’utilisateur pour la configuration des appels de groupe
description: Configuration requise pour les appels de groupe et droits d’utilisateur.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427872"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="eee40-103">Configuration requise pour les appels de groupe et droits d’utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eee40-103">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eee40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eee40-104">

<span> </span></span></span>

<span data-ttu-id="eee40-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="eee40-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="eee40-106">La cueillette de groupe est une fonctionnalité de gestion des appels qui est installée par défaut lors du déploiement d’Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="eee40-106">Group Call Pickup is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="eee40-107">Cette rubrique décrit ce que vous devez mettre en place avant de pouvoir configurer la collecte d’appels de groupe et les droits d’utilisateur nécessaires à l’exécution des tâches de configuration.</span><span class="sxs-lookup"><span data-stu-id="eee40-107">This topic describes what you need to have in place before you can configure Group Call Pickup and the user rights that you need to perform configuration tasks.</span></span>

<span data-ttu-id="eee40-108">Cette section part du principe que vous avez lu la documentation de planification liée au regroupement d’appels de groupe (voir [planification d’appels de groupe dans Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span><span class="sxs-lookup"><span data-stu-id="eee40-108">This section assumes that you have read the planning documentation related to Group Call Pickup (see [Planning for Group Call Pickup in Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span></span>

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a><span data-ttu-id="eee40-109">Configuration requise pour la configuration des appels de groupe</span><span class="sxs-lookup"><span data-stu-id="eee40-109">Group Call Pickup Configuration Prerequisites</span></span>

<span data-ttu-id="eee40-110">La collecte des appels de groupe nécessite les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="eee40-110">Group Call Pickup requires the following components:</span></span>

  - <span data-ttu-id="eee40-111">service d’application</span><span class="sxs-lookup"><span data-stu-id="eee40-111">Application service</span></span>

  - <span data-ttu-id="eee40-112">application de parcage d’appel</span><span class="sxs-lookup"><span data-stu-id="eee40-112">Call Park application</span></span>

<span data-ttu-id="eee40-113">Ces composants sont installés automatiquement lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="eee40-113">These components are installed automatically when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a><span data-ttu-id="eee40-114">Droits d’utilisateur de configuration des appels de groupe</span><span class="sxs-lookup"><span data-stu-id="eee40-114">Group Call Pickup Configuration User Rights</span></span>

<span data-ttu-id="eee40-115">Vous pouvez utiliser les outils d’administration suivants pour configurer la cueillette des appels de groupe :</span><span class="sxs-lookup"><span data-stu-id="eee40-115">You use the following administrative tools to configure Group Call Pickup:</span></span>

  - <span data-ttu-id="eee40-116">Lync Server Management Shell</span><span class="sxs-lookup"><span data-stu-id="eee40-116">Lync Server Management Shell</span></span>

  - <span data-ttu-id="eee40-117">Outil du kit de ressources SEFAUtil</span><span class="sxs-lookup"><span data-stu-id="eee40-117">SEFAUtil resource kit tool</span></span>

<span data-ttu-id="eee40-118">Utilisez Lync Server Management Shell pour créer et gérer des groupes de captures d’appels dans la table de stationnement d’appel.</span><span class="sxs-lookup"><span data-stu-id="eee40-118">Use Lync Server Management Shell to create and manage call pickup groups in the Call Park orbit table.</span></span> <span data-ttu-id="eee40-119">Utilisez l’outil de kit de ressources SEFAUtil pour attribuer un groupe de cueillette d’appel et activer le regroupement d’appels de groupe pour les utilisateurs ou pour désactiver la sélection d’appels de groupe pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="eee40-119">Use the SEFAUtil resource kit tool to assign a call pickup group and enable Group Call Pickup for users or to disable Group Call Pickup for users.</span></span>

<span data-ttu-id="eee40-120">La configuration de la cueillette de groupe nécessite l’un des rôles d’administration suivants, en fonction de la tâche :</span><span class="sxs-lookup"><span data-stu-id="eee40-120">Configuring Group Call Pickup requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="eee40-121">**CsVoiceAdministrator :** Ce rôle d’administrateur peut créer, configurer et gérer l’ensemble des stratégies et paramètres relatifs à la voix.</span><span class="sxs-lookup"><span data-stu-id="eee40-121">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="eee40-122">**CsUserAdministrator :** Ce rôle d’administrateur peut activer le prélèvement d’appels de groupe pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="eee40-122">**CsUserAdministrator:** This administrator role can enable Group Call Pickup for users.</span></span> <span data-ttu-id="eee40-123">Ce rôle d’administrateur dispose également d’un accès en lecture seule à toutes les configurations vocales.</span><span class="sxs-lookup"><span data-stu-id="eee40-123">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="eee40-124">**CsServerAdministrator :** Ce rôle d’administrateur peut gérer, surveiller et résoudre les problèmes liés aux serveurs et services.</span><span class="sxs-lookup"><span data-stu-id="eee40-124">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="eee40-125">**CsAdministrator :** Ce rôle d’administrateur peut effectuer toutes les tâches de CsVoiceAdministrator, CsServerAdministrator et CsUserAdministrator.</span><span class="sxs-lookup"><span data-stu-id="eee40-125">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="eee40-126">Pour plus d’informations sur les droits d’administration, voir <A href="lync-server-2013-planning-for-role-based-access-control.md">planification du contrôle d’accès basé sur les rôles dans Lync Server 2013</A> dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="eee40-126">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eee40-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eee40-127">See Also</span></span>


[<span data-ttu-id="eee40-128">Déploiement d’Enterprise Voice dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eee40-128">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="eee40-129">Planifier les fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eee40-129">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="eee40-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eee40-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

