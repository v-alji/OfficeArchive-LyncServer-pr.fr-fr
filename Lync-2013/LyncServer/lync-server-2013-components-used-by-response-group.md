---
title: 'Lync Server 2013 : Composants utilisés par Response Group'
description: 'Lync Server 2013 : composants utilisés par Response Group.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434556"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a><span data-ttu-id="c6ca5-103">Composants utilisés par Response Group dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c6ca5-103">Components used by Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6ca5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6ca5-104">

<span> </span></span></span>

<span data-ttu-id="c6ca5-105">_**Dernière modification de la rubrique :** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="c6ca5-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="c6ca5-106">L’application Response Group est activée automatiquement lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-106">The Response Group application is automatically enabled when you deploy Enterprise Voice.</span></span> <span data-ttu-id="c6ca5-107">Cette section décrit les composants qui prennent en charge l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-107">This section describes the components that support the Response Group application.</span></span>

<div>

## <a name="response-group-components"></a><span data-ttu-id="c6ca5-108">Composants de Response Group</span><span class="sxs-lookup"><span data-stu-id="c6ca5-108">Response Group Components</span></span>

<span data-ttu-id="c6ca5-109">Les composants Microsoft Lync Server 2013 suivants prennent en charge l’application Response Group :</span><span class="sxs-lookup"><span data-stu-id="c6ca5-109">The following Microsoft Lync Server 2013 components support the Response Group application:</span></span>

  - <span data-ttu-id="c6ca5-110">**Service d’application**   Le service d’application fournit une plateforme de déploiement, d’hébergement et de gestion d’applications de communications unifiées, telles que Response Group.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-110">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as Response Group.</span></span> <span data-ttu-id="c6ca5-111">Le service d’application est automatiquement installé sur chaque serveur frontal d’une grappe frontale et sur tous les serveurs Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-111">The Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="c6ca5-112">**Application Response Group**   L’application Response Group est l’une des applications de communications unifiées hébergées par le service d’application.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-112">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="c6ca5-113">Elle est incluse automatiquement lorsque vous déployez Response Group.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-113">It is included automatically when you deploy Response Group.</span></span> <span data-ttu-id="c6ca5-114">Le Response Group application route et met en file d’attente les appels entrants vers des groupes d’agents.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-114">The Response Group application routes and queues incoming calls to groups of agents.</span></span>

  - <span data-ttu-id="c6ca5-115">**Module linguistique**   Un module linguistique est requis pour la prise en charge de la reconnaissance vocale et de la synthèse vocale.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-115">**Language pack**   A language pack is required to support text-to-speech and speech recognition.</span></span> <span data-ttu-id="c6ca5-116">Ces technologies vocales servent lors de la configuration de messages (message de bienvenue et autres messages, ou les questions et réponses du système de réponse vocale interactive, par exemple).</span><span class="sxs-lookup"><span data-stu-id="c6ca5-116">These speech technologies are used when you configure messages, such as the welcome message and other prompts, and interactive voice response (IVR) questions and answers.</span></span> <span data-ttu-id="c6ca5-117">Par défaut, les 26 modules linguistiques pris en charge sont installés lors du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-117">By default, the 26 supported language packs are installed when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="c6ca5-118">**Fichiers audio**   Les fichiers audio sont utilisés pour les messages et la musique en attente.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-118">**Audio files**   Audio files are used for messages and on-hold music.</span></span>

  - <span data-ttu-id="c6ca5-119">**Magasin de fichiers**   Response Group utilise le stockage de fichiers pour stocker des fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-119">**File Store**   Response Group uses File store to store audio files.</span></span> <span data-ttu-id="c6ca5-120">Plusieurs pools de groupe de réponse peuvent utiliser la même instance du magasin de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-120">Multiple Response Group pools can use the same instance of File store.</span></span>

  - <span data-ttu-id="c6ca5-121">**Outil de configuration de Response Group**   L’outil de configuration de Response Group est un outil Web utilisé pour créer et configurer des groupes de réponse.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-121">**Response Group Configuration Tool**   The Response Group Configuration Tool is a web-based tool that is used to create and configure response groups.</span></span> <span data-ttu-id="c6ca5-122">L’outil de configuration de Response Group est inclus dans l’installation des services Web.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-122">The Response Group Configuration Tool is included when you install Web Services.</span></span>

  - <span data-ttu-id="c6ca5-123">**Panneau de configuration Microsoft Lync Server 2013**   Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer et configurer des groupes d’agents et des files d’attente pour les groupes de réponses.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-123">**Microsoft Lync Server 2013 Control Panel**   You can use Lync Server Control Panel to setup and configure agent groups and queues for response groups.</span></span>

  - <span data-ttu-id="c6ca5-124">**Lync Server Management Shell**   Tous les paramètres de Response Group peuvent être configurés à l’aide d’applets de applet Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-124">**Lync Server Management Shell**   All Response Group settings can be configured by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="c6ca5-125">**Microsoft Lync 2013**   Les agents officiels (agents nécessaires pour se connecter au groupe avant de pouvoir accepter les appels pour le groupe) utilisent Lync 2013 pour vous connecter au groupe et s’en déconnecter.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-125">**Microsoft Lync 2013**   Formal agents (agents who are required to sign in to the group before they can accept calls for the group) use Lync 2013 to sign in to and sign out from the group.</span></span> <span data-ttu-id="c6ca5-126">Si un groupe d’agent est configuré pour les agents officiels, les agents cliquent sur un élément de menu dans Lync 2013 pour ouvrir Internet Explorer et afficher une console de pages Web pour se connecter et s’en déconnecter.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-126">If an agent group is configured for formal agents, the agents click a menu item in Lync 2013 to open Internet Explorer and display a webpage console for signing in and out of the group.</span></span>

  - <span data-ttu-id="c6ca5-127">**Services Web**   Les services Web sont requis pour l’outil de configuration de Response Group, la console de connexion et de connexion des agents, le panneau de configuration de Lync Server et le service Web du client de Response Group.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-127">**Web Services**   Web Services is required for Response Group Configuration Tool, the agents’ sign-in and sign-out console, Lync Server Control Panel, and Response Group client web service.</span></span>

  - <span data-ttu-id="c6ca5-128">**Service Web du client de Response Group**   L’application Response Group fournit un service Web client qui peut être utilisé par des applications tierces pour récupérer des informations sur les agents, l’appartenance aux groupes d’agents, l’état de connexion des agents, le statut des appels pour les groupes et les groupes qui prennent en charge les appels anonymes.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-128">**Response Group Client Web Service**   Response Group application provides a client web service, which can be used by third-party applications to retrieve information about agents, agent group membership, agent sign-in status, call status for groups, and the groups that support anonymous calls.</span></span> <span data-ttu-id="c6ca5-129">Lync 2013 et Lync 2010 attendant utiliser le service Web du client de Response Group pour récupérer la liste des groupes de réponses que les agents peuvent utiliser pour effectuer des appels anonymes.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-129">Lync 2013 and Lync 2010 Attendant use Response Group Client Web service to retrieve the list of response groups that agents can use to make anonymous calls.</span></span> <span data-ttu-id="c6ca5-130">Le service Web client est inclus dans le cadre de l’installation des services Web.</span><span class="sxs-lookup"><span data-stu-id="c6ca5-130">The client web service is included when you install Web Services.</span></span>

<span data-ttu-id="c6ca5-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6ca5-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

