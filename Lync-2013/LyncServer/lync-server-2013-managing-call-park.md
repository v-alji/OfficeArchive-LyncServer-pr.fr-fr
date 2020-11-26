---
title: 'Lync Server 2013 : gestion du parc d’appels'
description: 'Lync Server 2013 : gestion du parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Call Park
ms:assetid: 9554cdf6-8e7c-48c8-94dd-f28e2befefdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688140(v=OCS.15)
ms:contentKeyID: 49733740
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6540cc6d4df06b3eaadd78dce8fe01990928045a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425968"
---
# <a name="managing-call-park-in-lync-server-2013"></a><span data-ttu-id="d5585-103">Gestion du parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5585-103">Managing Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5585-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5585-104">

<span> </span></span></span>

<span data-ttu-id="d5585-105">_**Dernière modification de la rubrique :** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="d5585-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="d5585-106">L’application de parc d’appels permet à un utilisateur de voix entreprise de mettre un appel en attente à partir d’un téléphone, puis de récupérer l’appel plus tard depuis n’importe quel téléphone.</span><span class="sxs-lookup"><span data-stu-id="d5585-106">The Call Park application enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later from any telephone.</span></span> <span data-ttu-id="d5585-107">Lorsque l’utilisateur travaille sur un appel, Lync Server transfère l’appel vers un numéro temporaire, appelé *orbite*, où l’appel est maintenu jusqu’à ce que quelqu’un le récupère.</span><span class="sxs-lookup"><span data-stu-id="d5585-107">When the user parks a call, Lync Server transfers the call to a temporary number, called an *orbit*, where the call is held until someone retrieves it or it times out.</span></span>

<span data-ttu-id="d5585-108">Les rubriques de cette section fournissent des procédures pas à pas pour les tâches que vous pouvez effectuer pour personnaliser et mettre à jour l’application de parc d’appels dans votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="d5585-108">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Call Park application in your deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d5585-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d5585-109">In This Section</span></span>

  - [<span data-ttu-id="d5585-110">Configurer les extensions de numéro de téléphone pour les appels de parking dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5585-110">Configure phone number extensions for parking calls in Lync Server 2013</span></span>](lync-server-2013-configure-phone-number-extensions-for-parking-calls.md)

  - [<span data-ttu-id="d5585-111">Configurer les paramètres de parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5585-111">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="d5585-112">Personnaliser le parc d’appels en attente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5585-112">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="d5585-113">Gestion du parcage d’appel lors de la récupération d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5585-113">Manage Call Park during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-call-park-during-disaster-recovery.md)

<span data-ttu-id="d5585-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5585-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

