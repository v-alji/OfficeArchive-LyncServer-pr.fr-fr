---
title: 'Lync Server 2013 : déploiement de fonctionnalités de gestion des appels'
description: 'Lync Server 2013 : déploiement de fonctionnalités de gestion des appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430069"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="f01a1-103">Déploiement de fonctionnalités de gestion des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f01a1-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f01a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f01a1-104">

<span> </span></span></span>

<span data-ttu-id="f01a1-105">_**Dernière modification de la rubrique :** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="f01a1-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="f01a1-106">Les fonctionnalités de gestion des appels voix entreprise contrôlent la façon dont les appels entrants sont routés et répondent.</span><span class="sxs-lookup"><span data-stu-id="f01a1-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="f01a1-107">Lync Server 2013 fournit les fonctionnalités de gestion des appels suivantes :</span><span class="sxs-lookup"><span data-stu-id="f01a1-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="f01a1-108">**Park d’appel :** Permet aux utilisateurs vocaux de parcer temporairement un appel et de le décrocher sur le même téléphone ou sur un autre téléphone.</span><span class="sxs-lookup"><span data-stu-id="f01a1-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="f01a1-109">**Capture de groupe :** Permet aux utilisateurs de répondre aux appels passés à un autre utilisateur qui est affecté à un groupe de collecte en composant le numéro de groupe de capture d’appel.</span><span class="sxs-lookup"><span data-stu-id="f01a1-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="f01a1-110">**Response Group :** Achemine les appels entrants vers des groupes d’agents en utilisant des groupes de recherche ou des questions et réponses de réponse vocale interactives.</span><span class="sxs-lookup"><span data-stu-id="f01a1-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="f01a1-111">**Annonce :** Lit un message pour les appels passés vers un numéro non attribué, ou route l’appel à un autre endroit, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f01a1-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="f01a1-112">Cette section décrit comment configurer ces fonctionnalités de gestion des appels dans le cadre d’un déploiement voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="f01a1-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f01a1-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f01a1-113">In This Section</span></span>

  - [<span data-ttu-id="f01a1-114">Configuration du parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f01a1-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="f01a1-115">Configuration de la collecte d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f01a1-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="f01a1-116">Configuration du groupe Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f01a1-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="f01a1-117">Configuration des annonces pour les numéros non affectés dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f01a1-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="f01a1-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f01a1-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

