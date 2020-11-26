---
title: Introduction
description: Place.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438742"
---
# <a name="introduction"></a><span data-ttu-id="f765e-103">Introduction</span><span class="sxs-lookup"><span data-stu-id="f765e-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f765e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f765e-104">

<span> </span></span></span>

<span data-ttu-id="f765e-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="f765e-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="f765e-106">L’outil de stress et de performance de Lync Server 2013 (appelé LyncPerfTool) peut simuler la charge utilisateur des types suivants :</span><span class="sxs-lookup"><span data-stu-id="f765e-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f765e-107">Messagerie instantanée et présence</span><span class="sxs-lookup"><span data-stu-id="f765e-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="f765e-108">Audioconférence</span><span class="sxs-lookup"><span data-stu-id="f765e-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f765e-109">Partage d'application</span><span class="sxs-lookup"><span data-stu-id="f765e-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="f765e-110">Voix sur IP (VoIP), y compris la simulation de réseau téléphonique commuté (PSTN)</span><span class="sxs-lookup"><span data-stu-id="f765e-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f765e-111">Conférences de clients d’accès Web</span><span class="sxs-lookup"><span data-stu-id="f765e-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="f765e-112">Microsoft Lync 2013 attendant</span><span class="sxs-lookup"><span data-stu-id="f765e-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f765e-113">Response Groups</span><span class="sxs-lookup"><span data-stu-id="f765e-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="f765e-114">Extension de liste de distribution</span><span class="sxs-lookup"><span data-stu-id="f765e-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f765e-115">Requête de téléchargement du carnet d’adresses et du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="f765e-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="f765e-116">9-1-1 d’amélioration (E9-1-1) : profil d’emplacement et d’emplacement (plan de numérotation)</span><span class="sxs-lookup"><span data-stu-id="f765e-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f765e-117">Multivue</span><span class="sxs-lookup"><span data-stu-id="f765e-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="f765e-118">Affichage de plusieurs flux d’une conférence</span><span class="sxs-lookup"><span data-stu-id="f765e-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f765e-119">L’outil de stress et de performance de Lync Server 2013 prend en charge la génération et la Fédération par pool via la configuration avancée uniquement.</span><span class="sxs-lookup"><span data-stu-id="f765e-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="f765e-120">L’outil ne simule pas non plus la charge des utilisateurs pour les clients suivants :</span><span class="sxs-lookup"><span data-stu-id="f765e-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="f765e-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="f765e-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="f765e-122">Conversation permanente Lync 2013</span><span class="sxs-lookup"><span data-stu-id="f765e-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="f765e-123">Par conséquent, l’outil de stress et de performance de Lync Server 2013 ne prend pas en charge le test des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="f765e-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="f765e-124">Conversation permanente Lync 2013</span><span class="sxs-lookup"><span data-stu-id="f765e-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="f765e-125">Scénarios d’intégration Exchange</span><span class="sxs-lookup"><span data-stu-id="f765e-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="f765e-126">Applications et fichiers inclus dans l’outil de stress et de performance de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f765e-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="f765e-127">Les applications suivantes sont incluses dans l’outil de stress et de performance de Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="f765e-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f765e-128">Il</span><span class="sxs-lookup"><span data-stu-id="f765e-128">Tool</span></span></th>
<th><span data-ttu-id="f765e-129">Description</span><span class="sxs-lookup"><span data-stu-id="f765e-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f765e-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="f765e-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="f765e-131">Outil de mise en service des utilisateurs de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f765e-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="f765e-132">Cet outil permet de créer des utilisateurs et des contacts.</span><span class="sxs-lookup"><span data-stu-id="f765e-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f765e-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="f765e-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="f765e-134">Outil de configuration de chargement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f765e-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="f765e-135">Cet outil permet de configurer les caractéristiques de la charge d’utilisateur pour la simulation.</span><span class="sxs-lookup"><span data-stu-id="f765e-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f765e-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="f765e-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="f765e-137">Outil de stress et de performance de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f765e-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="f765e-138">LyncPerfTool est l’outil qui simule la charge utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f765e-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f765e-139">Default. TMX</span><span class="sxs-lookup"><span data-stu-id="f765e-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="f765e-140">Default. TMX est requis pour l’utilisation de l’outil de journalisation Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f765e-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f765e-141">Exemples de scripts de mise en service</span><span class="sxs-lookup"><span data-stu-id="f765e-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="f765e-142">Ces exemples sont utilisés pour configurer la topologie pour exécuter des tests de charge, en fonction de scénarios spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f765e-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f765e-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f765e-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

