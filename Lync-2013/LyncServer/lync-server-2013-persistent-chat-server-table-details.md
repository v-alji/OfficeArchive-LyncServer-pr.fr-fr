---
title: 'Lync Server 2013 : Détails de la table des serveurs de conversation permanente'
description: 'Lync Server 2013 : détails sur la table serveur Chat permanent.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server table details
ms:assetid: c22d4a76-da50-49de-9038-e0ed7b8e1b58
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615034(v=OCS.15)
ms:contentKeyID: 48185323
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a27feaaccf861d537127f06920cf903be5ae000
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443082"
---
# <a name="persistent-chat-server-table-details-in-lync-server-2013"></a><span data-ttu-id="418aa-103">Détails de la table des serveurs de conversation permanente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-103">Persistent Chat Server table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="418aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="418aa-104">

<span> </span></span></span>

<span data-ttu-id="418aa-105">_**Dernière modification de la rubrique :** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="418aa-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="418aa-106">Les rubriques suivantes décrivent en détail les colonnes dans chaque table de schéma de base de données de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="418aa-106">The following topics detail the columns in each of the Persistent Chat database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="418aa-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="418aa-107">In This Section</span></span>

  - [<span data-ttu-id="418aa-108">tblADCookie dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-108">tblADCookie in Lync Server 2013</span></span>](lync-server-2013-tbladcookie.md)

  - [<span data-ttu-id="418aa-109">tblPrincipalMemberDifference dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-109">tblPrincipalMemberDifference in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmemberdifference.md)

  - [<span data-ttu-id="418aa-110">tblADUpdates dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-110">tblADUpdates in Lync Server 2013</span></span>](lync-server-2013-tbladupdates.md)

  - [<span data-ttu-id="418aa-111">tblPrincipalMembers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-111">tblPrincipalMembers in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmembers.md)

  - [<span data-ttu-id="418aa-112">tblPrincipalMeta dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-112">tblPrincipalMeta in Lync Server 2013</span></span>](lync-server-2013-tblprincipalmeta.md)

  - [<span data-ttu-id="418aa-113">tblSkippedAffiliations dans Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-113">tblSkippedAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblskippedaffiliations.md)

  - [<span data-ttu-id="418aa-114">tblPrincipalType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-114">tblPrincipalType in Lync Server 2013</span></span>](lync-server-2013-tblprincipaltype.md)

  - [<span data-ttu-id="418aa-115">tblPrincipal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-115">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)

  - [<span data-ttu-id="418aa-116">tblPrincipalAffiliations dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-116">tblPrincipalAffiliations in Lync Server 2013</span></span>](lync-server-2013-tblprincipalaffiliations.md)

  - [<span data-ttu-id="418aa-117">tblNode dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-117">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)

  - [<span data-ttu-id="418aa-118">tblRoleType dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-118">tblRoleType in Lync Server 2013</span></span>](lync-server-2013-tblroletype.md)

  - [<span data-ttu-id="418aa-119">tblScopePrincipal dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-119">tblScopePrincipal in Lync Server 2013</span></span>](lync-server-2013-tblscopeprincipal.md)

  - [<span data-ttu-id="418aa-120">tblPrincipalRole dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-120">tblPrincipalRole in Lync Server 2013</span></span>](lync-server-2013-tblprincipalrole.md)

  - [<span data-ttu-id="418aa-121">tblSiopWhiteList dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-121">tblSiopWhiteList in Lync Server 2013</span></span>](lync-server-2013-tblsiopwhitelist.md)

  - [<span data-ttu-id="418aa-122">tblEnumAttribute dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-122">tblEnumAttribute in Lync Server 2013</span></span>](lync-server-2013-tblenumattribute.md)

  - [<span data-ttu-id="418aa-123">tblEnumValue dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-123">tblEnumValue in Lync Server 2013</span></span>](lync-server-2013-tblenumvalue.md)

  - [<span data-ttu-id="418aa-124">tblPrincipalInvites dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-124">tblPrincipalInvites in Lync Server 2013</span></span>](lync-server-2013-tblprincipalinvites.md)

  - [<span data-ttu-id="418aa-125">tblChat dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-125">tblChat in Lync Server 2013</span></span>](lync-server-2013-tblchat.md)

  - [<span data-ttu-id="418aa-126">tblLastInviteId dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-126">tblLastInviteId in Lync Server 2013</span></span>](lync-server-2013-tbllastinviteid.md)

  - [<span data-ttu-id="418aa-127">tblLastChatId dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-127">tblLastChatId in Lync Server 2013</span></span>](lync-server-2013-tbllastchatid.md)

  - [<span data-ttu-id="418aa-128">tblPreference dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-128">tblPreference in Lync Server 2013</span></span>](lync-server-2013-tblpreference.md)

  - [<span data-ttu-id="418aa-129">tblFileToken dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-129">tblFileToken in Lync Server 2013</span></span>](lync-server-2013-tblfiletoken.md)

  - [<span data-ttu-id="418aa-130">tblServerIdentity dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-130">tblServerIdentity in Lync Server 2013</span></span>](lync-server-2013-tblserveridentity.md)

  - [<span data-ttu-id="418aa-131">tblAdminLock dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-131">tblAdminLock in Lync Server 2013</span></span>](lync-server-2013-tbladminlock.md)

  - [<span data-ttu-id="418aa-132">tblSystemRevision dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-132">tblSystemRevision in Lync Server 2013</span></span>](lync-server-2013-tblsystemrevision.md)

  - [<span data-ttu-id="418aa-133">tblActivePeers dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-133">tblActivePeers in Lync Server 2013</span></span>](lync-server-2013-tblactivepeers.md)

  - [<span data-ttu-id="418aa-134">tblConfig dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-134">tblConfig in Lync Server 2013</span></span>](lync-server-2013-tblconfig.md)

  - [<span data-ttu-id="418aa-135">tblComplianceData dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-135">tblComplianceData in Lync Server 2013</span></span>](lync-server-2013-tblcompliancedata.md)

  - [<span data-ttu-id="418aa-136">tblComplianceFanout dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-136">tblComplianceFanout in Lync Server 2013</span></span>](lync-server-2013-tblcompliancefanout.md)

  - [<span data-ttu-id="418aa-137">tblComplianceParticipant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-137">tblComplianceParticipant in Lync Server 2013</span></span>](lync-server-2013-tblcomplianceparticipant.md)

  - [<span data-ttu-id="418aa-138">tblComplianceState dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="418aa-138">tblComplianceState in Lync Server 2013</span></span>](lync-server-2013-tblcompliancestate.md)

<span data-ttu-id="418aa-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="418aa-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

