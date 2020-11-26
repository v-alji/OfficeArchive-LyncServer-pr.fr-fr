---
title: 'Lync Server 2013 : prise en charge de grandes réunions'
description: 'Lync Server 2013 : prise en charge de réunions importantes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supporting large meetings using Lync Server
ms:assetid: 509a424f-a33d-4e72-8f87-a3ec7bb1ddeb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204894(v=OCS.15)
ms:contentKeyID: 48184136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e116f4668c37fd26eea5cec322a8c6483385e7d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441409"
---
# <a name="supporting-large-meetings-using-lync-server-2013"></a><span data-ttu-id="9fe5e-103">Prise en charge de grandes réunions à l’aide de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fe5e-103">Supporting large meetings using Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9fe5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9fe5e-104">

<span> </span></span></span>

<span data-ttu-id="9fe5e-105">_**Dernière modification de la rubrique :** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="9fe5e-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="9fe5e-106">Les grandes réunions ne suivent pas le modèle de test décrit dans la section précédente, car ils présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fe5e-106">Large meetings do not follow the test model described in the previous section because they have the following characteristics:</span></span>

  - <span data-ttu-id="9fe5e-107">Le format de la réunion est celui d’une présentation un-à-plusieurs.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-107">The meeting format is a one-to-many presentation.</span></span>

  - <span data-ttu-id="9fe5e-108">Un ou plusieurs utilisateurs sont des présentateurs. Le reste de l’assistance sont des participants.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-108">One or a few users are presenters, and everyone else participates only as attendees.</span></span>

  - <span data-ttu-id="9fe5e-109">Le partage de présentation PowerPoint est la principale activité de collaboration pour les données.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-109">PowerPoint presentation sharing is the main data collaboration activity.</span></span>

  - <span data-ttu-id="9fe5e-110">L’audio est nécessaire et la vidéo peut également être utilisée.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-110">Audio is required and video may also be used.</span></span>

  - <span data-ttu-id="9fe5e-111">En règle générale, une personne dédiée, qui est l’organisateur de la réunion ou un Assistant, organise la réunion à l’avance.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-111">A dedicated person, generally either the meeting organizer or an assistant to the organizer sets up the meeting well in advance.</span></span>

  - <span data-ttu-id="9fe5e-112">Le personnel dédié (et non les présentateurs) est chargé de mener la réunion, notamment en ce qui concerne la connexion à une réunion en ligne, la vérification du bon fonctionnement de l’audio, de la vidéo et du partage des diapositives, la gestion de la salle d’attente et des rôles utilisateurs, l’activation ou la désactivation du son des participants, la gestion des questions, ainsi que la gestion des enregistrements, de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-112">Dedicated staff (not the presenters) runs the meeting, including connecting to an online meeting, verifying that audio, video, and slide sharing work, managing lobby and user roles, muting and unmuting participants, taking questions, and managing recordings, as appropriate.</span></span>

<span data-ttu-id="9fe5e-113">La prise en charge de grandes réunions d’un maximum de 1000 utilisateurs nécessite de traiter les problèmes liés au modèle de matériel partagé et au modèle sans réservation.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-113">Supporting large meetings of up to 1000 users requires addressing the issues related to both the shared hardware model and the no-reservation model.</span></span>

<span data-ttu-id="9fe5e-114">Pour disposer de suffisamment de ressources aux niveaux du processeur et de la mémoire pour les réunions incluant jusqu’à 1 000 utilisateurs, les serveurs frontaux d’hébergement ne doivent pas gérer de fonctionnalités de messagerie instantanée et de présence, ni de charges de travail liées à Voix Entreprise.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-114">To have sufficient CPU and memory resources for meetings of up to 1000 users, the hosting Front End Servers should not host any other instant messaging (IM) and presence or Enterprise Voice workloads.</span></span> <span data-ttu-id="9fe5e-115">Elle ne doit pas non plus accueillir d’autres réunions, quelle que soit la taille des autres réunions.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-115">It should also not host any other meetings, regardless of the size of the other meetings.</span></span> <span data-ttu-id="9fe5e-116">Cela signifie que les réunions d’hébergement d’un maximum de 1000 utilisateurs nécessitent de configurer un pool Lync Server distinct destiné à accueillir des réunions de grande envergure de plus de 1000 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-116">This means that hosting meetings of up to 1000 users requires setting up a separate Lync Server pool that is dedicated to hosting large meetings of up to 1000 users.</span></span>

<span data-ttu-id="9fe5e-117">Dans le cas d’un pool de serveurs Lync dédié à l’hébergement de réunions de grande taille, il est conseillé de n’organiser qu’une seule réunion d’au maximum 1000 utilisateurs, ce qui permet de réserver une réunion à l’avance à l’aide d’un processus de planification hors bande pour garantir une prise en charge dédiée du serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-117">A Lync Server pool that is dedicated to hosting large meetings should host one and only one meeting of up to 1000 users at the same time, so meeting times need to be reserved in advance via an out of band scheduling process to ensure dedicated support from the Front End Servers.</span></span> <span data-ttu-id="9fe5e-118">Pour prendre en charge plusieurs réunions de grande envergure en même temps, nous vous recommandons de configurer plusieurs pools de réunions volumineux dédiées.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-118">To support more than one large meeting at the same time, we recommend setting up multiple dedicated large-meeting pools.</span></span>

<span data-ttu-id="9fe5e-119">Nous recommandons qu’une personne dédiée exécute et contrôle la partie en ligne d’une grande réunion.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-119">We recommend that a dedicated person run and monitor the online portion of a large meeting.</span></span> <span data-ttu-id="9fe5e-120">Il peut s’agir de l’organisateur, du délégué de l’organisateur ou du présentateur ou d’un membre de l’équipe de support technique dédiée de grande réunion, selon les préférences de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-120">This person might be the organizer, delegate of the organizer or presenter, or a member of the dedicated large meeting support team, depending on the organization’s preferences.</span></span>

<span data-ttu-id="9fe5e-121">Dans les sections suivantes, nous décrivons comment implémenter un pool dédié pour les réunions de grande envergure, y compris des pratiques recommandées pour l’utilisation de Lync Server 2013 pour prendre en charge des scénarios de réunion importants.</span><span class="sxs-lookup"><span data-stu-id="9fe5e-121">In the following sections, we describe how to implement a dedicated pool for large meetings, including best practices for using Lync Server 2013 to support large meeting scenarios.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9fe5e-122">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9fe5e-122">In This Section</span></span>

  - [<span data-ttu-id="9fe5e-123">Configuration de la prise en charge des réunions de grande envergure dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fe5e-123">Setting up support for large meetings in Lync Server 2013</span></span>](lync-server-2013-setting-up-support-for-large-meetings.md)

  - [<span data-ttu-id="9fe5e-124">Gérer des réunions de grande envergure dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9fe5e-124">Managing large meetings in Lync Server 2013</span></span>](lync-server-2013-managing-large-meetings.md)

<span data-ttu-id="9fe5e-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9fe5e-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

