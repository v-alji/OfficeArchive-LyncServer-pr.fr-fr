---
title: 'Lync Server 2013 : Planification du serveur de conversation permanente'
description: 'Lync Server 2013 : planification du serveur de chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Persistent Chat Server
ms:assetid: 57b2f574-234e-4a5a-bb78-8823369ba79e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398381(v=OCS.15)
ms:contentKeyID: 48184190
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6944437492a1eee718a614369201c3548c95864a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424451"
---
# <a name="planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="35097-103">Planification du serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-103">Planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="35097-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="35097-104">

<span> </span></span></span>

<span data-ttu-id="35097-105">_**Dernière modification de la rubrique :** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="35097-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="35097-106">Vous pouvez utiliser Lync Server 2013, serveur de chat permanent pour permettre à plusieurs utilisateurs de participer à des conversations dans lesquelles ils publient et accèdent au contenu de rubriques spécifiques, y compris le texte, les liens et les fichiers.</span><span class="sxs-lookup"><span data-stu-id="35097-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="35097-107">Bien que les utilisateurs puissent communiquer en temps réel pendant une session, le contenu de chaque session est permanent, ce qui signifie qu’il reste disponible après la fin d’une session.</span><span class="sxs-lookup"><span data-stu-id="35097-107">Although users can communicate in real time during a session, the content of each session is persistent, which means it continues to be available after a session ends.</span></span>

<span data-ttu-id="35097-108">Cette section décrit les considérations relatives à la planification dans un serveur Lync Server 2013, le déploiement de serveur Chat permanent, y compris la définition des exigences, l’identification des composants et des topologies prises en charge, et des recommandations en matière de déploiement.</span><span class="sxs-lookup"><span data-stu-id="35097-108">This section describes planning considerations in a Lync Server 2013, Persistent Chat Server deployment, including defining requirements, identifying components and supported topologies, and deployment recommendations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="35097-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="35097-109">In This Section</span></span>

  - [<span data-ttu-id="35097-110">Vue d’ensemble du serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-110">Overview of Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-overview-of-persistent-chat-server.md)

  - [<span data-ttu-id="35097-111">Fonctionnement du serveur Chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-111">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="35097-112">Définition de la configuration requise pour l’organisation du serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-112">Defining your organization's requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="35097-113">Composants et topologies pour le serveur de chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-113">Components and topologies for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-persistent-chat-server.md)

  - [<span data-ttu-id="35097-114">Configuration requise pour le serveur de chat permanent dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-114">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="35097-115">Configuration des systèmes et de l’infrastructure pour le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-115">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="35097-116">Liste de vérification du déploiement pour le serveur de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="35097-116">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

<span data-ttu-id="35097-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="35097-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

