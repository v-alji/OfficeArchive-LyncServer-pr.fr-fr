---
title: 'Lync Server 2013 : Définition de la configuration requise pour les appels d’urgence'
description: 'Lync Server 2013 : définition de votre configuration requise pour les appels d’urgence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for emergency calls
ms:assetid: 5c12b517-9be6-41d0-83e2-11c78793620c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398404(v=OCS.15)
ms:contentKeyID: 48184276
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d3c9908dcb4008a1442af86971e42eb4096a98b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430832"
---
# <a name="defining-your-requirements-for-emergency-calls-in-lync-server-2013"></a><span data-ttu-id="97c06-103">Définition de la configuration requise pour les appels d’urgence dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-103">Defining your requirements for emergency calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97c06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97c06-104">

<span> </span></span></span>

<span data-ttu-id="97c06-105">_**Dernière modification de la rubrique :** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="97c06-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="97c06-106">Avant de commencer un déploiement de Microsoft Lync Server 2013 E9-1-1, vous devez d’abord répondre aux questions détaillées des sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="97c06-106">Before you begin a Microsoft Lync Server 2013 E9-1-1 deployment, you should first be able to answer the questions detailed in the following sections.</span></span> <span data-ttu-id="97c06-107">La planification dont vous avez besoin dépend du type de solution E9-1-1 que vous choisissez de déployer : fournisseur de services E9-1-1 de jonction SIP ou numéro ELIN (Emergency Location Identification Number).</span><span class="sxs-lookup"><span data-stu-id="97c06-107">The planning you need to do depends on the type of E9-1-1 solution that you choose to deploy—a SIP trunk E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway.</span></span> <span data-ttu-id="97c06-108">Le tableau ci-dessous identifie les sections du document de planification à consulter pour chacune de ces solutions.</span><span class="sxs-lookup"><span data-stu-id="97c06-108">The following table identifies the sections in this planning workbook that you’ll need to review for each of those solutions.</span></span>

### <a name="planning-steps-by-type-of-e9-1-1-solution"></a><span data-ttu-id="97c06-109">Étapes de planification par type de solution E9-1-1</span><span class="sxs-lookup"><span data-stu-id="97c06-109">Planning Steps by Type of E9-1-1 Solution</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97c06-110">Fournisseur de services de jonction SIP</span><span class="sxs-lookup"><span data-stu-id="97c06-110">SIP trunk service provider</span></span></th>
<th><span data-ttu-id="97c06-111">Passerelle ELIN</span><span class="sxs-lookup"><span data-stu-id="97c06-111">ELIN gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97c06-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Définition de l’étendue du déploiement E9-1-1 dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Définition de l’étendue du déploiement E9-1-1 dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c06-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Définition des éléments réseau utilisés pour déterminer l’emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Définition des éléments réseau utilisés pour déterminer l’emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c06-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Activation des utilisateurs pour E9-1-1 dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Activation des utilisateurs pour E9-1-1 dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c06-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Gestion des emplacements pour les fournisseurs de services SIP Trunk dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Managing locations for SIP trunk service providers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Gestion des emplacements pour les passerelles ELIN dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Managing locations for ELIN gateways in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c06-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Définition de l’interface utilisateur pour l’acquisition manuelle d’un emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Définition de l’interface utilisateur pour l’acquisition manuelle d’un emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c06-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Designing the SIP Trunk pour E9-1-1 dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Designing the SIP trunk for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-123"><a href="lync-server-2013-including-the-security-desk.md">Inclure le centre de sécurité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-123"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c06-124"><a href="lync-server-2013-including-the-security-desk.md">Inclure le centre de sécurité dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-124"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-125"><a href="lync-server-2013-defining-the-location-policy.md">Définition de la stratégie d’emplacement pour Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-125"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c06-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Choix d’un fournisseur de services E9-1-1 pour Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Choosing an E9-1-1 service provider for Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="97c06-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Attribution de l’étendue de la stratégie d’emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97c06-128"><a href="lync-server-2013-defining-the-location-policy.md">Définition de la stratégie d’emplacement pour Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-128"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97c06-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Attribution de l’étendue de la stratégie d’emplacement dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="97c06-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="97c06-130">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="97c06-130">In This Section</span></span>

  - [<span data-ttu-id="97c06-131">Définition de l’étendue du déploiement E9-1-1 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-131">Defining the scope of the E9-1-1 deployment in Lync Server 2013</span></span>](lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md)

  - [<span data-ttu-id="97c06-132">Définition des éléments réseau utilisés pour déterminer l’emplacement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-132">Defining the network elements used to determine location in Lync Server 2013</span></span>](lync-server-2013-defining-the-network-elements-used-to-determine-location.md)

  - [<span data-ttu-id="97c06-133">Activation des utilisateurs pour E9-1-1 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-133">Enabling users for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-enabling-users-for-e9-1-1.md)

  - [<span data-ttu-id="97c06-134">Gestion des emplacements pour les fournisseurs de services SIP Trunk dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-134">Managing locations for SIP trunk service providers in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-sip-trunk-service-providers.md)

  - [<span data-ttu-id="97c06-135">Gestion des emplacements pour les passerelles ELIN dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-135">Managing locations for ELIN gateways in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-elin-gateways.md)

  - [<span data-ttu-id="97c06-136">Définition de l’interface utilisateur pour l’acquisition manuelle d’un emplacement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-136">Defining the user experience for manually acquiring a location in Lync Server 2013</span></span>](lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md)

  - [<span data-ttu-id="97c06-137">Designing the SIP Trunk pour E9-1-1 dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-137">Designing the SIP trunk for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md)

  - [<span data-ttu-id="97c06-138">Inclure le centre de sécurité dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-138">Including the security desk in Lync Server 2013</span></span>](lync-server-2013-including-the-security-desk.md)

  - [<span data-ttu-id="97c06-139">Choix d’un fournisseur de services E9-1-1 pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-139">Choosing an E9-1-1 service provider for Lync Server 2013</span></span>](lync-server-2013-choosing-an-e9-1-1-service-provider.md)

  - [<span data-ttu-id="97c06-140">Définition de la stratégie d’emplacement pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-140">Defining the location policy for Lync Server 2013</span></span>](lync-server-2013-defining-the-location-policy.md)

  - [<span data-ttu-id="97c06-141">Attribution de l’étendue de la stratégie d’emplacement dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97c06-141">Assigning location policy scope in Lync Server 2013</span></span>](lync-server-2013-assigning-location-policy-scope.md)

<span data-ttu-id="97c06-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97c06-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

