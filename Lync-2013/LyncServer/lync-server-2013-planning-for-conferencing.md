---
title: 'Lync Server 2013 : Planification des conférences'
description: 'Lync Server 2013 : planification de conférences.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for conferencing
ms:assetid: 983a272a-e1b3-4d70-8f84-836b092fe526
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398781(v=OCS.15)
ms:contentKeyID: 48184937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28e71d185b7be8971c451351aac60dcaaf7eaeda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443019"
---
# <a name="planning-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="1cee9-103">Planification des conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-103">Planning for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cee9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cee9-104">

<span> </span></span></span>

<span data-ttu-id="1cee9-105">_**Dernière modification de la rubrique :** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="1cee9-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="1cee9-106">Lync Server 2013 offre de nombreuses fonctionnalités de conférence :</span><span class="sxs-lookup"><span data-stu-id="1cee9-106">Lync Server 2013 offers a rich set of conferencing capabilities:</span></span>

  - <span data-ttu-id="1cee9-107">Conférences Web, notamment la collaboration sur des documents, le partage d’application et le partage de bureau.</span><span class="sxs-lookup"><span data-stu-id="1cee9-107">Web conferencing, which includes document collaboration, application sharing, and desktop sharing.</span></span> <span data-ttu-id="1cee9-108">Lync Server 2013 utilise Office Web Apps et Office Web Apps Server pour gérer le partage et le rendu des présentations PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="1cee9-108">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="1cee9-109">Pour plus d’informations sur l’installation et la configuration d’Office Web Apps Server, reportez-vous à la rubrique [configuration de l’intégration avec Office Web Apps Server et Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="1cee9-109">For details about installing and configuring the Office Web Apps Server, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

  - <span data-ttu-id="1cee9-110">Les conférences audio/vidéo (A/V), qui permettent aux utilisateurs de disposer de conférences audio ou vidéo en temps réel sans recourir à des services externes tels que le service Microsoft Live Meeting ou un pont audio tiers.</span><span class="sxs-lookup"><span data-stu-id="1cee9-110">Audio/video (A/V) conferencing, which enables users to have real-time audio or video conferences without the need for external services such as the Microsoft Live Meeting service or a third-party audio bridge.</span></span>

  - <span data-ttu-id="1cee9-111">Conférence rendez-vous, qui permet aux utilisateurs d’accéder à la partie audio d’une conférence 2013 Server Lync à l’aide d’un téléphone réseau téléphonique commuté (PSTN) sans nécessiter un fournisseur de services d’audioconférence tiers.</span><span class="sxs-lookup"><span data-stu-id="1cee9-111">Dial-in conferencing, which allows users to join the audio portion of a Lync Server 2013 conference by using a public switched telephone network (PSTN) phone without requiring a third-party audio conferencing provider.</span></span>

  - <span data-ttu-id="1cee9-112">Conférences de messagerie instantanée, dans lesquelles plus de deux parties communiquent au sein d’une seule et même session de messagerie instantanée.</span><span class="sxs-lookup"><span data-stu-id="1cee9-112">Instant messaging (IM) conferencing, in which more than two parties communicate in a single IM session.</span></span> <span data-ttu-id="1cee9-113">Pour plus d’informations sur les conférences de messagerie instantanée, voir [planification pour les serveurs frontaux, la messagerie instantanée et la présence dans Lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="1cee9-113">For details about IM conferencing, see [Planning for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="1cee9-114">Lync Server 2013 prend en charge les conférences planifiées et les conférences impromptues.</span><span class="sxs-lookup"><span data-stu-id="1cee9-114">Lync Server 2013 supports both scheduled conferences and impromptu conferences.</span></span>

<span data-ttu-id="1cee9-115">Lorsque vous déployez Lync Server 2013, serveur frontal, vous pouvez choisir de déployer également les fonctionnalités de conférence Web, de conférence A/V et de conférence rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="1cee9-115">When you deploy Lync Server 2013, Front End Server, you can choose whether to also deploy the web conferencing, A/V conferencing, and dial-in conferencing capabilities.</span></span> <span data-ttu-id="1cee9-116">Les fonctionnalités de conférence par messagerie instantanée sont toujours déployées automatiquement avec les fonctionnalités de conversation par messagerie instantanée sur les serveurs frontaux Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1cee9-116">IM conferencing capabilities are always automatically deployed along with IM conversation capabilities on Lync Server 2013 Front End Servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1cee9-117">Si votre déploiement inclut des réunions organisées à l’aide de clients Office Communicator 2007 R2 (y compris la console Live Meeting ou le complément de conférence pour Microsoft Office Outlook), les limitations suivantes seront appliquées après leur migration vers Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="1cee9-117">If your deployment includes meetings organized using Office Communicator 2007 R2 clients (including the Live Meeting console or Conferencing Add-in for Microsoft Office Outlook), the meetings will have the following limitations after they are migrated to Lync Server 2013:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="1cee9-118">Les utilisateurs de la réunion ne seront pas en mesure d’utiliser les fonctionnalités de collaboration de données, notamment la collaboration sur des documents, le partage d’application et le partage de bureau.</span><span class="sxs-lookup"><span data-stu-id="1cee9-118">Users in the meeting will not be able to use data collaboration features, including document collaboration, application sharing, and desktop sharing.</span></span></P>
> <LI>
> <P><span data-ttu-id="1cee9-119">Des problèmes de stabilité peuvent se produire car les clients Office Communicator 2007 R2 ne sont pas pris en charge avec Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1cee9-119">Stability issues may arise since Office Communicator 2007 R2 clients are not supported with Lync Server 2013.</span></span></P></LI></UL><span data-ttu-id="1cee9-120">Pour éviter ces problèmes, replanifiez une réunion organisée à l’aide de clients Office Communicator 2007 R2 avec Outlook 2010 ou Outlook 2013 à l’aide du complément réunion en ligne pour Lync 2010 ou d’une réunion en ligne pour Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="1cee9-120">To avoid these issues, reschedule any meeting organized using Office Communicator 2007 R2 clients with Outlook 2010 or Outlook 2013 using either the Online Meeting Add-in for Lync 2010 or Online Meeting Add-in for Lync 2013.</span></span>



</div>

<span data-ttu-id="1cee9-121">Les sections suivantes décrivent ce qui est requis pour déployer les différents types de fonctionnalités de conférences, dont le processus de planification, les composants, les configurations matérielles et logicielles et le processus de déploiement.</span><span class="sxs-lookup"><span data-stu-id="1cee9-121">The following sections describe what is required to deploy the various types of conferencing capabilities, including the planning process, components, hardware and software requirements, and the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1cee9-122">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1cee9-122">In This Section</span></span>

  - [<span data-ttu-id="1cee9-123">Vue d’ensemble des conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-123">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)

  - [<span data-ttu-id="1cee9-124">Définition de la configuration requise pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-124">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)

  - [<span data-ttu-id="1cee9-125">Composants et topologies utilisés pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-125">Components and topologies for conferencing in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-conferencing.md)

  - [<span data-ttu-id="1cee9-126">Configuration technique requise pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-126">Technical requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-conferencing.md)

  - [<span data-ttu-id="1cee9-127">Liste de vérification du déploiement pour les conférences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-127">Deployment checklist for conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-conferencing.md)

  - [<span data-ttu-id="1cee9-128">Prise en charge des réunions importantes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cee9-128">Support for large meetings in Lync Server 2013</span></span>](lync-server-2013-support-for-large-meetings.md)

<span data-ttu-id="1cee9-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cee9-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

