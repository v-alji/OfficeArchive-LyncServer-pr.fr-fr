---
title: Configurer des règles de code confidentiel (PIN) pour les conférences rendez-vous
description: Configurer des règles de code confidentiel (PIN) pour les conférences rendez-vous.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial-in conferencing personal identification number (PIN) rules
ms:assetid: 27b79fb1-e2dc-4f71-bc82-b6eb61be2b16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520967(v=OCS.15)
ms:contentKeyID: 48183668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 799092ba57e9a85cd196840fc81c1f46b96e9900
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395136"
---
# <a name="configure-dial-in-conferencing-personal-identification-number-pin-rules-in-lync-server-2013"></a><span data-ttu-id="5928e-103">Configurer des règles de code confidentiel (PIN) de conférence rendez-vous dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5928e-103">Configure dial-in conferencing personal identification number (PIN) rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5928e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5928e-104">

<span> </span></span></span>

<span data-ttu-id="5928e-105">_**Dernière modification de la rubrique :** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="5928e-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="5928e-106">Les utilisateurs de Lync Server 2013 disposant d’informations d’identification AD DS (Active Directory Domain Services) au sein de votre organisation peuvent participer à des conférences rendez-vous en tant qu’utilisateurs authentifiés à l’aide d’un code confidentiel (PIN).</span><span class="sxs-lookup"><span data-stu-id="5928e-106">Lync Server 2013 users who have Active Directory Domain Services (AD DS) credentials in your organization can join dial-in conferences as authenticated users by using a personal identification number (PIN).</span></span> <span data-ttu-id="5928e-107">La stratégie de code confidentiel définit le fonctionnement des codes confidentiels d’accès aux conférences rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="5928e-107">PIN policy defines the rules for how dial-in conferencing PINs work.</span></span>

<span data-ttu-id="5928e-108">Vous pouvez en créer une si vous voulez qu’une stratégie spécifique s’applique à un site ou à un groupe d’utilisateurs spécifique.</span><span class="sxs-lookup"><span data-stu-id="5928e-108">You can create a new PIN policy if you want a specific policy to apply to a site or to a certain group of users.</span></span> <span data-ttu-id="5928e-109">Si vous voulez utiliser la même stratégie de code confidentiel au sein de toute votre organisation, vous pouvez utiliser la stratégie de code confidentiel globale et la modifier, au besoin.</span><span class="sxs-lookup"><span data-stu-id="5928e-109">If you want to use the same PIN policy for your entire organization, you can use the global PIN policy and modify it as needed.</span></span> <span data-ttu-id="5928e-110">Les stratégies de code confidentiel s’appliquent aux utilisateurs, de l’étendue la plus petite à l’étendue la plus grande.</span><span class="sxs-lookup"><span data-stu-id="5928e-110">PIN policies apply to users from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="5928e-111">Si vous affectez une stratégie de code confidentiel au niveau utilisateur, ces paramètres prévalent.</span><span class="sxs-lookup"><span data-stu-id="5928e-111">If you assign a user-level PIN policy to a user, those settings take precedence.</span></span> <span data-ttu-id="5928e-112">Si vous n’affectez pas de stratégie au niveau utilisateur, la stratégie de code confidentiel de niveau site s’applique, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="5928e-112">If you do not assign a user policy, the site-level PIN policy applies, if it exists.</span></span> <span data-ttu-id="5928e-113">En l’absence de stratégie de niveau utilisateur ou site, les paramètres par défaut de la stratégie de code confidentiel globale sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="5928e-113">If no user or site policies apply, global PIN policy provides the default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5928e-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5928e-114">In This Section</span></span>

  - [<span data-ttu-id="5928e-115">Modification des paramètres de code confidentiel des conférences rendez-vous par défaut dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5928e-115">Modify the default dial-in conferencing PIN settings in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-dial-in-conferencing-pin-settings.md)

  - [<span data-ttu-id="5928e-116">Création ou modification des paramètres de code confidentiel dans Lync Server 2013 pour les conférences rendez-vous pour un site ou un groupe d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5928e-116">Create or modify dial-in conferencing PIN settings in Lync Server 2013 for a site or group of users</span></span>](lync-server-2013-create-or-modify-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

  - [<span data-ttu-id="5928e-117">Supprimer les paramètres de code confidentiel de conférence rendez-vous pour un site ou un groupe d’utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5928e-117">Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013</span></span>](lync-server-2013-delete-dial-in-conferencing-pin-settings-for-a-site-or-group-of-users.md)

<span data-ttu-id="5928e-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5928e-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

