---
title: 'Lync Server 2013 : Processus de déploiement pour l’intégration de la messagerie unifiée Exchange hébergée'
description: 'Lync Server 2013 : processus de déploiement pour l’intégration de la messagerie unifiée Exchange hébergée.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for integrating hosted Exchange UM with Lync Server
ms:assetid: dbec9c38-7f66-419d-b8c3-c61380052cac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398968(v=OCS.15)
ms:contentKeyID: 48185586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 83239c6534dfdaa65109c8880cc4cb4946bffab6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429677"
---
# <a name="deployment-process-for-integrating-hosted-exchange-um-with-lync-server-2013"></a><span data-ttu-id="bad64-103">Processus de déploiement pour l’intégration de la messagerie unifiée Exchange hébergée à Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bad64-103">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bad64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bad64-104">

<span> </span></span></span>

<span data-ttu-id="bad64-105">_**Dernière modification de la rubrique :** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="bad64-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="bad64-106">La planification efficace de l’intégration de Lync Server 2013 à la messagerie unifiée Exchange hébergée (MU) nécessite que vous prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bad64-106">Effective planning for integrating Lync Server 2013 with hosted Exchange Unified Messaging (UM) requires that you take into account the following:</span></span>

  - <span data-ttu-id="bad64-107">Conditions préalables à l’intégration de Lync Server 2013 avec la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="bad64-107">Prerequisites for integrating Lync Server 2013 with hosted Exchange UM</span></span>

  - <span data-ttu-id="bad64-108">Étapes requises lors du processus d’intégration</span><span class="sxs-lookup"><span data-stu-id="bad64-108">Steps required during the integration process</span></span>

<div>

## <a name="deployment-prerequisites-for-integrating-with-hosted-exchange-um"></a><span data-ttu-id="bad64-109">Prérequis de déploiement pour l’intégration à la messagerie unifiée Exchange hébergée</span><span class="sxs-lookup"><span data-stu-id="bad64-109">Deployment Prerequisites for Integrating with Hosted Exchange UM</span></span>

<span data-ttu-id="bad64-110">Avant de pouvoir commencer le processus d’intégration, vous devez déjà avoir déployé Lync Server 2013 (au minimum, un pool frontal ou un serveur Standard Edition Server), un serveur Edge et des clients Lync 2013 ou Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="bad64-110">Before you can begin the integration process, you must already have deployed Lync Server 2013 (at a minimum, a Front End pool or a Standard Edition server), an Edge Server, and Lync 2013 or Lync 2010 clients.</span></span>

</div>

<div>

## <a name="integration-process"></a><span data-ttu-id="bad64-111">Processus d’intégration</span><span class="sxs-lookup"><span data-stu-id="bad64-111">Integration Process</span></span>

<span data-ttu-id="bad64-112">Le tableau suivant fournit une vue d’ensemble du processus d’intégration d’Exchange UM hébergé.</span><span class="sxs-lookup"><span data-stu-id="bad64-112">The following table provides an overview of the hosted Exchange UM integration process.</span></span> <span data-ttu-id="bad64-113">Pour plus d’informations sur les étapes de déploiement, voir [fourniture de messages vocaux aux utilisateurs Lync Server 2013 sur la messagerie unifiée Exchange hébergée](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md) dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="bad64-113">For details about deployment steps, see [Providing Lync Server 2013 users voice mail on hosted Exchange UM](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bad64-114">Phase</span><span class="sxs-lookup"><span data-stu-id="bad64-114">Phase</span></span></th>
<th><span data-ttu-id="bad64-115">Étapes</span><span class="sxs-lookup"><span data-stu-id="bad64-115">Steps</span></span></th>
<th><span data-ttu-id="bad64-116">Droits et autorisations</span><span class="sxs-lookup"><span data-stu-id="bad64-116">Rights and permissions</span></span></th>
<th><span data-ttu-id="bad64-117">Documentation de déploiement</span><span class="sxs-lookup"><span data-stu-id="bad64-117">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bad64-118">Configurer le serveur de périphérie</span><span class="sxs-lookup"><span data-stu-id="bad64-118">Configure the Edge Server.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="bad64-119">Configurez le serveur Edge pour la fédération.</span><span class="sxs-lookup"><span data-stu-id="bad64-119">Configure the Edge Server for federation.</span></span></p></li>
<li><p><span data-ttu-id="bad64-120">Répliquer manuellement les données sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="bad64-120">Manually replicate data to the Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="bad64-121">Configurez le fournisseur d’hébergement sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="bad64-121">Configure the hosting provider on the Edge Server.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="bad64-122">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="bad64-122">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="bad64-123"><a href="lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md">Configuration du serveur Edge pour l’intégration à la messagerie unifiée Exchange hébergée</a></span><span class="sxs-lookup"><span data-stu-id="bad64-123"><a href="lync-server-2013-configure-the-edge-server-for-integration-with-hosted-exchange-um.md">Configure the Edge Server for integration with hosted Exchange UM</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bad64-124">Configurer une stratégie de messagerie vocale hébergée.</span><span class="sxs-lookup"><span data-stu-id="bad64-124">Configure hosted voice mail policy.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="bad64-125">Modifiez la stratégie globale de messagerie vocale hébergée ou créez une nouvelle stratégie de messagerie vocale hébergée avec l’étendue site ou Per-User.</span><span class="sxs-lookup"><span data-stu-id="bad64-125">Either modify the global hosted voice mail policy or create a new hosted voice mail policy with Site or Per-User scope.</span></span></p></li>
<li><p><span data-ttu-id="bad64-126">Dans le cas d’une stratégie avec l’étendue Per-User, affectez la stratégie à des utilisateurs ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="bad64-126">For policies with Per-User scope, assign the policy to users or groups.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="bad64-127">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="bad64-127">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="bad64-128"><a href="lync-server-2013-manage-hosted-voice-mail-policies.md">Gestion des stratégies de messagerie vocale hébergée dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="bad64-128"><a href="lync-server-2013-manage-hosted-voice-mail-policies.md">Manage hosted voice mail policies in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bad64-129">Autorisez les utilisateurs à utiliser la messagerie vocale hébergée.</span><span class="sxs-lookup"><span data-stu-id="bad64-129">Enable users for hosted voice mail.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="bad64-130">Configurez des comptes d’utilisateurs pour les utilisateurs dont la boîte aux lettres se trouve sur un service Exchange hébergé.</span><span class="sxs-lookup"><span data-stu-id="bad64-130">Configure user accounts for users whose mailboxes are on a hosted Exchange service.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="bad64-131">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="bad64-131">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="bad64-132"><a href="lync-server-2013-enable-users-for-hosted-voice-mail.md">Activation des utilisateurs pour la messagerie vocale hébergée dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="bad64-132"><a href="lync-server-2013-enable-users-for-hosted-voice-mail.md">Enable users for hosted voice mail in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bad64-133">Configurer les objets de contact hébergés.</span><span class="sxs-lookup"><span data-stu-id="bad64-133">Configure hosted contact objects.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="bad64-134">Créer des objets de contact de standard automatique pour la messagerie unifiée Exchange hébergée.</span><span class="sxs-lookup"><span data-stu-id="bad64-134">Create auto-attendant Contact objects for hosted Exchange UM.</span></span></p></li>
<li><p><span data-ttu-id="bad64-135">Créer des objets de contact d’accès d’abonné pour la messagerie unifiée Exchange hébergée.</span><span class="sxs-lookup"><span data-stu-id="bad64-135">Create Subscriber Access contact objects for hosted Exchange UM.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="bad64-136">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="bad64-136">RTCUniversalUserAdmins</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="bad64-137">Pour créer, modifier ou supprimer des objets de contact, l’utilisateur exécutant l’applet de commande New-CsExUmContact, Set-CsExUmContact ou Remove-CsExUmContact doit disposer de l’autorisation appropriée pour l’unité d’organisation Active Directory où les nouveaux objets de contact sont stockés.</span><span class="sxs-lookup"><span data-stu-id="bad64-137">To create, modify or remove contact objects, the user who runs the New-CsExUmContact, Set-CsExUmContact or Remove-CsExUmContact cmdlet must have the correct permission to the Active Directory organizational unit where the new contact objects are stored.</span></span> <span data-ttu-id="bad64-138">Cette autorisation peut être accordée en exécutant l’applet de commande Grant-CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="bad64-138">This permission can be granted by running the Grant-CsOUPermission cmdlet.</span></span> <span data-ttu-id="bad64-139">Pour plus d’informations, reportez-vous à la documentation Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="bad64-139">For details, see the Lync Server Management Shell documentation.</span></span>


</div></td>
<td><p><span data-ttu-id="bad64-140"><a href="lync-server-2013-create-contact-objects-for-hosted-exchange-um.md">Création des objets de contact pour la messagerie unifiée Exchange hébergée dans Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="bad64-140"><a href="lync-server-2013-create-contact-objects-for-hosted-exchange-um.md">Create contact objects for hosted Exchange UM in Lync Server 2013</a></span></span></p></td><span data-ttu-id="bad64-141">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bad64-141">
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

