---
title: 'Lync Server 2013 : Activation d’une stratégie de serveur de conversation permanente'
description: 'Lync Server 2013 : activer la stratégie de serveur de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Persistent Chat Server policy
ms:assetid: 87063d6c-2e38-4970-b76d-2aa15f0de29e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205056(v=OCS.15)
ms:contentKeyID: 48184718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58da577679795f00492af72b43ca72106d40f4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428838"
---
# <a name="enable-persistent-chat-server-policy-in-lync-server-2013"></a><span data-ttu-id="df70d-103">Activation d’une stratégie de serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df70d-103">Enable Persistent Chat Server policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df70d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df70d-104">

<span> </span></span></span>

<span data-ttu-id="df70d-105">_**Dernière modification de la rubrique :** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="df70d-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="df70d-106">Dans le panneau de configuration de Lync Server 2013, vous pouvez utiliser la page de **stratégie de chat permanent** du groupe de **conversation permanente** pour gérer les stratégies au niveau global, de pool, de site ou d’utilisateur, y compris la configuration de la stratégie globale par défaut et la création d’une ou plusieurs stratégies d’utilisateur et de site supplémentaires pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="df70d-106">In the Lync Server 2013 Control Panel, you can use the **Persistent Chat Policy** page of the **Persistent Chat** group to manage policies at a global, pool, site, or user level, including configuring the default global policy and creating one or more additional user and site policies for your deployment.</span></span> <span data-ttu-id="df70d-107">Si un utilisateur est activé pour le serveur Chat permanent par stratégie, l’environnement serveur Chat permanent apparaît dans le client Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="df70d-107">If a user is enabled for Persistent Chat Server by policy, then the Persistent Chat Server environment appears in their Lync 2013 client.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="df70d-108">Dans la topologie, les stratégies de site serveur de chat permanent s’appliquent globalement, le pool de chaque utilisateur, le site de chaque utilisateur ou par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df70d-108">In the topology, Persistent Chat Server site policies apply globally, per user’s pool, or per user’s site, or per user.</span></span>



</div>

<span data-ttu-id="df70d-109">La stratégie globale est créée automatiquement lorsque vous déployez le serveur Chat permanent et qu’elle peut être configurée, mais pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="df70d-109">The global policy is created automatically when you deploy Persistent Chat Server, and it can be configured, but not deleted.</span></span> <span data-ttu-id="df70d-110">Comme la stratégie globale s’appliquent à tous les utilisateurs, il n’est pas obligatoire de la définir par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="df70d-110">Because the global policy applies to all users, it doesn’t have to be set per user.</span></span>

<span data-ttu-id="df70d-111">Vous pouvez créer et configurer plusieurs stratégies de site et utilisateurs qui, conjointement avec la stratégie globale, permettent aux utilisateurs de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="df70d-111">You can create and configure multiple site and user policies which, together with the global policy, enable users for Persistent Chat Server.</span></span> <span data-ttu-id="df70d-112">Les stratégies de serveur de chat permanent de pool et de site remplacent la stratégie de serveur de chat permanent global, mais uniquement pour les utilisateurs de ce site.</span><span class="sxs-lookup"><span data-stu-id="df70d-112">Pool and site Persistent Chat Server policies override the global Persistent Chat Server policy, but only for users of that site.</span></span> <span data-ttu-id="df70d-113">Les stratégies utilisateur remplacent les stratégies utilisateur, de pool et globales pour les utilisateurs auxquels la stratégie utilisateur est affectée.</span><span class="sxs-lookup"><span data-stu-id="df70d-113">User policies override both global, pool, and site policies for the users to whom the user policy is assigned.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="df70d-114">Pour configurer et utiliser le serveur de chat permanent, vous devez d’abord utiliser le générateur de topologie pour ajouter la prise en charge du serveur de chat permanent à la topologie, puis publier la topologie.</span><span class="sxs-lookup"><span data-stu-id="df70d-114">To configure and use Persistent Chat Server, you must first use Topology Builder to add Persistent Chat Server support to the topology, and then publish the topology.</span></span> <span data-ttu-id="df70d-115">Pour plus d’informations, reportez-vous à la rubrique <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Ajouter un serveur Chat permanent à votre déploiement dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="df70d-115">For details, see <A href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="df70d-116">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="df70d-116">In This Section</span></span>

  - [<span data-ttu-id="df70d-117">Configuration de la stratégie globale pour la conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df70d-117">Configure the global policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-configure-the-global-policy-for-persistent-chat.md)

  - [<span data-ttu-id="df70d-118">Création d’une stratégie de site pour la conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df70d-118">Create a site policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-site-policy-for-persistent-chat.md)

  - [<span data-ttu-id="df70d-119">Création d’une stratégie utilisateur pour la conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df70d-119">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

  - [<span data-ttu-id="df70d-120">Application d’une stratégie de conversation permanente à un utilisateur ou à un groupe d’utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df70d-120">Apply a Persistent Chat policy to a user or user group in Lync Server 2013</span></span>](lync-server-2013-apply-a-persistent-chat-policy-to-a-user-or-user-group.md)

<span data-ttu-id="df70d-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df70d-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

