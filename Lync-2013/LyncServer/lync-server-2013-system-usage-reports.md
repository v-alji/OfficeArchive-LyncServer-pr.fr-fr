---
title: 'Lync Server 2013 : rapports d’utilisation du système'
description: 'Lync Server 2013 : rapports d’utilisation du système.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System usage reports
ms:assetid: 187d316d-2456-417e-b636-05527a18ef06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558618(v=OCS.15)
ms:contentKeyID: 48183529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fffaf22dacbc68958e64090fd4c7d44e32f8ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423553"
---
# <a name="system-usage-reports-in-lync-server-2013"></a><span data-ttu-id="fbb31-103">Rapports sur l’utilisation du système dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-103">System usage reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbb31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbb31-104">

<span> </span></span></span>

<span data-ttu-id="fbb31-105">_**Dernière modification de la rubrique :** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="fbb31-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="fbb31-106">Les rapports d’utilisation du système fournissent des informations sur l’utilisation du système en fonction des données d’enregistrement des détails des appels collectées par le serveur Lync.</span><span class="sxs-lookup"><span data-stu-id="fbb31-106">The System Usage Reports provide system usage information based on call detail recording (CDR) data collected by the Lync Server.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="fbb31-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fbb31-107">In This Section</span></span>

  - [<span data-ttu-id="fbb31-108">Rapport sur l’inscription des utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-108">User Registration Report in Lync Server 2013</span></span>](lync-server-2013-user-registration-report.md)
    
    <span data-ttu-id="fbb31-109">Fournit un résumé de la connectivité utilisateur au déploiement de Lync Server 2013 en fonction des événements d’inscription, tels que les connexions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fbb31-109">Provides a summary of user connectivity to the Lync Server 2013 deployment based on registration events such as user logons.</span></span> <span data-ttu-id="fbb31-110">Ce rapport fournit un moyen d’afficher à la fois des ouvertures de session internes et externes, et de comparer le nombre d’utilisateurs connectés à Lync Server 2013 et le nombre d’utilisateurs qui ont réellement utilisé le service pendant la connexion.</span><span class="sxs-lookup"><span data-stu-id="fbb31-110">The report provides a way to view both internal and external logons, and to compare the number of users who logged on to Lync Server 2013 with the number of users who actually used the service while they were logged on.</span></span>

  - [<span data-ttu-id="fbb31-111">Rapport de synthèse des activités d’égal à égal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-111">Peer-to-Peer Activity Summary Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-summary-report.md)
    
    <span data-ttu-id="fbb31-p102">Fournit une synthèse des sessions de messagerie instantanée P2P, audio, vidéo, de transfert de fichiers et de partage d’applications. Les sessions P2P sont des sessions impliquant seulement deux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fbb31-p102">Provides a summary of peer-to-peer instant messaging (IM), audio, video, file transfer, and application sharing sessions. Peer-to-peer sessions are sessions involving just two users.</span></span>

  - [<span data-ttu-id="fbb31-114">Rapport de synthèse de conférence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-114">Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-conference-summary-report.md)
    
    <span data-ttu-id="fbb31-115">Fournit une synthèse de toutes les activités de conférence.</span><span class="sxs-lookup"><span data-stu-id="fbb31-115">Provides a summary of all conference activities.</span></span> <span data-ttu-id="fbb31-116">Les conférences sont des sessions qui impliquent plus de deux personnes.</span><span class="sxs-lookup"><span data-stu-id="fbb31-116">Conferences are sessions involving three or more people.</span></span>

  - [<span data-ttu-id="fbb31-117">Rapport de synthèse des conférences RTC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-117">PSTN Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-pstn-conference-summary-report.md)
    
    <span data-ttu-id="fbb31-p104">Fournit une synthèse de toutes les conférences RTC. Il s’agit de conférences où au moins un utilisateur compose un numéro sur le réseau téléphonique commuté (RTC). Ces conférences sont aussi appelées *conférence rendez-vous*.</span><span class="sxs-lookup"><span data-stu-id="fbb31-p104">Provides a summary of all PSTN conferences. These are conferences where at least one user dials in using the public switched telephone network (PSTN), which is also referred to as *dial-in conferencing*.</span></span>

  - [<span data-ttu-id="fbb31-120">Rapport sur l’utilisation du groupe de réponses dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-120">Response Group Usage Report in Lync Server 2013</span></span>](lync-server-2013-response-group-usage-report.md)
    
    <span data-ttu-id="fbb31-121">Fournit un résumé de l’utilisation de Response Group.</span><span class="sxs-lookup"><span data-stu-id="fbb31-121">Provides a summary of Response Group usage.</span></span> <span data-ttu-id="fbb31-122">L’application Response Group vous permet d’acheminer automatiquement les appels téléphoniques vers des entités comme un support technique ou une ligne d’assistance clientèle.</span><span class="sxs-lookup"><span data-stu-id="fbb31-122">The Response Group application provides a way for you to automatically route phone calls to entities such as a help desk or customer support line.</span></span>

  - [<span data-ttu-id="fbb31-123">Rapport d’inventaire des téléphones IP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-123">IP Phone Inventory Report in Lync Server 2013</span></span>](lync-server-2013-ip-phone-inventory-report.md)
    
    <span data-ttu-id="fbb31-124">Fournit des informations sur les téléphones IP actuellement en cours d’utilisation dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="fbb31-124">Provides information about the IP phones currently in use in the organization.</span></span> <span data-ttu-id="fbb31-125">Le rapport est basé sur les inscriptions et les connexions des téléphones.</span><span class="sxs-lookup"><span data-stu-id="fbb31-125">The report is based on phone registrations and logons.</span></span> <span data-ttu-id="fbb31-126">Il ne doit pas être considéré comme un inventaire complet.</span><span class="sxs-lookup"><span data-stu-id="fbb31-126">It should not be considered a complete inventory.</span></span> <span data-ttu-id="fbb31-127">Par exemple, vous ne possédez peut-être plus certains téléphones qui sont encore répertoriés dans le rapport (car ils se sont connectés au moins une fois).</span><span class="sxs-lookup"><span data-stu-id="fbb31-127">For example, you might have removed phones that are still listed in the report because they logged on at least once.</span></span> <span data-ttu-id="fbb31-128">De même, il est possible que vous ayez de nouveaux téléphones qui ne s’affichent pas dans le rapport, car les utilisateurs ne sont pas encore connectés à Lync Server avec leur nouveau téléphone.</span><span class="sxs-lookup"><span data-stu-id="fbb31-128">Likewise, you might also have new phones that do not show up in the report simply because users have not logged on to Lync Server with their new phones yet.</span></span>

  - [<span data-ttu-id="fbb31-129">Rapport de contrôle d’admission des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbb31-129">Call Admission Control Report in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-report.md)
    
    <span data-ttu-id="fbb31-p107">Fournit une liste d’activités P2P et de conférence qui utilisent le contrôle d’admission des appels. Le contrôle d’admission des appels (CAC, Call Admission Control) permet de déterminer si les sessions de communication en temps réel, comme les appels audio et vidéo, doivent ou non être autorisées, en fonction des restrictions de bande passante.</span><span class="sxs-lookup"><span data-stu-id="fbb31-p107">Provides a list of peer-to-peer and conference activities that use call admission control. Call admission control (CAC) is a way of determining whether you should allow real-time communications sessions, such as voice or video calls, based on bandwidth constraints.</span></span>

<span data-ttu-id="fbb31-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbb31-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

