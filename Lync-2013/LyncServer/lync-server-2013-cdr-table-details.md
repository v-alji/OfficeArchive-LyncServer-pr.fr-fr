---
title: 'Lync Server 2013 : Informations sur la table des enregistrements des détails des appels'
description: 'Lync Server 2013 : détails sur la table CDR.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435480"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="b1b08-103">Informations sur la table des enregistrements des détails des appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1b08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1b08-104">

<span> </span></span></span>

<span data-ttu-id="b1b08-105">_**Dernière modification de la rubrique :** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="b1b08-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="b1b08-106">Les rubriques suivantes décrivent en détail les colonnes dans chaque table de schéma de la base de données d’enregistrements des détails des appels.</span><span class="sxs-lookup"><span data-stu-id="b1b08-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b1b08-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b1b08-107">In This Section</span></span>

  - [<span data-ttu-id="b1b08-108">Table Application dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="b1b08-109">Table CallPriorities dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="b1b08-110">Table CallType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="b1b08-111">Table ClientVersions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="b1b08-112">Table ConferenceJoinTimeThresholds dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="b1b08-113">Table ConferenceMessageCount dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="b1b08-114">Table Conferences dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="b1b08-115">Table ConferenceSessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="b1b08-116">Table ConferenceUris dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="b1b08-117">Table ContentTypes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="b1b08-118">Table DeRegisterType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="b1b08-119">Table Devices dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="b1b08-120">Table Dialogs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="b1b08-121">Table EdgeServers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="b1b08-122">Table ErrorCategory dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="b1b08-123">Table ErrorDef dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="b1b08-124">Table ErrorReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="b1b08-125">Table FileTransfers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="b1b08-126">Table FocusJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="b1b08-127">Table frontale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="b1b08-128">Table Gateways dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="b1b08-129">Table HardwareVersions dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="b1b08-130">Table IMReportSummary dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="b1b08-131">Table Locations dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="b1b08-132">Table Manufacturers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="b1b08-133">Table McuJoinsAndLeaves dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="b1b08-134">Table Mcus dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="b1b08-135">Table Media dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="b1b08-136">Table MediaList dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="b1b08-137">Table MediationServers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="b1b08-138">Table MSMQProcessing dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="b1b08-139">Table !Phones dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="b1b08-140">Table Pools dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="b1b08-141">Table ProgressReport dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="b1b08-142">Table PurgeSettings dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="b1b08-143">Table Registration dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="b1b08-144">Table Roles dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="b1b08-145">Table Servers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="b1b08-146">Table SessionDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="b1b08-147">Table SIPResponseMetaData dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="b1b08-148">Table syndicators dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="b1b08-149">Table SyndicatorsTenantMap dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="b1b08-150">Tableau de tâches dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="b1b08-151">Table Tenants dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="b1b08-152">Table UriTypes dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="b1b08-153">Table Users dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="b1b08-154">Table UserAgentDef dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="b1b08-155">Table UserStatistics dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="b1b08-156">Table VoipDetails dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1b08-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="b1b08-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1b08-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

