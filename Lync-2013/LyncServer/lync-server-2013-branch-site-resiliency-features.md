---
title: 'Lync Server 2013 : Fonctionnalités de résistance de site de succursale'
description: 'Lync Server 2013 : fonctionnalités de résilience de succursale.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Branch-site resiliency features
ms:assetid: 8e3feda5-9a38-4e3c-b808-af29f19c5eb9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398715(v=OCS.15)
ms:contentKeyID: 48184765
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a498751ce99d0e8e85d6cbe53915c864e64440bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436019"
---
# <a name="branch-site-resiliency-features-in-lync-server-2013"></a><span data-ttu-id="f6f3c-103">Fonctionnalités de résistance de site de succursale dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6f3c-103">Branch-site resiliency features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6f3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6f3c-104">

<span> </span></span></span>

<span data-ttu-id="f6f3c-105">_**Dernière modification de la rubrique :** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="f6f3c-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="f6f3c-106">Si vous fournissez la résistance des sites de succursale et que la connexion de réseau étendu d’un site de succursale à un site central échoue si ce dernier est inaccessible, les fonctionnalités vocales suivantes seront encore disponibles :</span><span class="sxs-lookup"><span data-stu-id="f6f3c-106">If you provide branch-site resiliency, if a branch site’s WAN connection to a central site fails or if the central site is unreachable, the following voice features should continue to be available:</span></span>

<div>


  - <span data-ttu-id="f6f3c-107">Appels RTC entrants et sortants</span><span class="sxs-lookup"><span data-stu-id="f6f3c-107">Inbound and outbound public switched telephone network (PSTN) calls</span></span>

  - <span data-ttu-id="f6f3c-108">Appels Enterprise entre des utilisateurs situés sur le même site ou sur deux sites différents</span><span class="sxs-lookup"><span data-stu-id="f6f3c-108">Enterprise calls between users at both the same site and between two different sites</span></span>

  - <span data-ttu-id="f6f3c-109">Fonctionnalités de base de gestion des appels, dont la mise en attente, la récupération et le transfert</span><span class="sxs-lookup"><span data-stu-id="f6f3c-109">Basic call handling, including call hold, retrieval, and transfer</span></span>

  - <span data-ttu-id="f6f3c-110">Messagerie instantanée entre deux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f6f3c-110">Two-party instant messaging</span></span>

  - <span data-ttu-id="f6f3c-111">Services de transfert d’appel, de sonnerie simultanée des points de terminaison, de délégation d’appel et d’appel d’équipe, mais seulement si le délégant et le délégué (par exemple, un responsable et l’administrateur de ce dernier), ou tous les membres de l’équipe, sont configurés sur le même site.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-111">Call forwarding, simultaneous ringing of endpoints, call delegation, and team call services, but only if the delegator and delegate (for example, a manager and the manager’s administrator), or all team members, are configured at the same site</span></span>

  - <span data-ttu-id="f6f3c-112">Enregistrements des détails des appels (CDR)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-112">Call detail records (CDRs)</span></span>

  - <span data-ttu-id="f6f3c-113">Conférence rendez-vous par réseau téléphonique commuté (RTC) avec standard automatique de conférence</span><span class="sxs-lookup"><span data-stu-id="f6f3c-113">PSTN dial-in conferencing with Conferencing Auto-Attendant</span></span>

  - <span data-ttu-id="f6f3c-114">Fonctionnalités de messagerie vocale si vous configurez les paramètres de réacheminement de la messagerie vocale.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-114">Voice mail capabilities, if you configure voice mail rerouting settings.</span></span> <span data-ttu-id="f6f3c-115">(Pour plus d’informations, consultez [Configuration requise pour la résilience du site de succursale pour Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-115">(For details, see [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).)</span></span>

  - <span data-ttu-id="f6f3c-116">Authentification et autorisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f6f3c-116">User authentication and authorization</span></span>

<span data-ttu-id="f6f3c-117">Les fonctionnalités suivantes ne seront disponibles que si votre solution de résilience est un déploiement de Lync Server à une échelle complète sur le site de la succursale :</span><span class="sxs-lookup"><span data-stu-id="f6f3c-117">The following features will be available only if your resiliency solution is a full-scale Lync Server deployment at the branch site:</span></span>

  - <span data-ttu-id="f6f3c-118">Messagerie instantanée, conférence A/V et web</span><span class="sxs-lookup"><span data-stu-id="f6f3c-118">IM, web, and A/V conferencing</span></span>

  - <span data-ttu-id="f6f3c-119">Routage basé sur la présence et Ne pas déranger (DND (quand les appels ne sonnent pas sur les postes dont le statut est Ne pas déranger)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-119">Presence and Do Not Disturb (DND)-based routing (where calls are prevented from ringing on extensions that have DND activated)</span></span>

  - <span data-ttu-id="f6f3c-120">Mise à jour des paramètres de transfert d’appel</span><span class="sxs-lookup"><span data-stu-id="f6f3c-120">Updating call forwarding settings</span></span>

  - <span data-ttu-id="f6f3c-121">Application de groupe de réponse et application de parc d’appels</span><span class="sxs-lookup"><span data-stu-id="f6f3c-121">Response Group application and Call Park application</span></span>

  - <span data-ttu-id="f6f3c-122">Attribution de nouveaux téléphones et clients, mais uniquement si les services de domaine Active Directory sont présents au niveau du site de succursale.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-122">Provisioning new phones and clients, but only if Active Directory Domain Services is present at the branch site.</span></span>

  - <span data-ttu-id="f6f3c-123">Enhanced 9-1-1 (E9-1-1)</span><span class="sxs-lookup"><span data-stu-id="f6f3c-123">Enhanced 9-1-1 (E9-1-1)</span></span>
    
    <span data-ttu-id="f6f3c-124">Si E9-1-1 est déployé et que le Trunk SIP sur le site central n’est pas disponible parce que la liaison WAN est en panne, l’application branche Survivable achemine les appels E9-1-1 vers la passerelle locale.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-124">If E9-1-1 is deployed, and the SIP trunk at the central site is not available because the WAN link is down, then the Survivable Branch Appliance will route E9-1-1 calls to the local branch gateway.</span></span> <span data-ttu-id="f6f3c-125">Pour activer cette fonctionnalité, les stratégies de voix des utilisateurs du site de succursale doivent acheminer les appels vers la passerelle locale en cas de panne du réseau étendu (WAN).</span><span class="sxs-lookup"><span data-stu-id="f6f3c-125">To enable this feature, the branch-site users’ voice policies should route calls to the local gateway in the event of WAN failure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f6f3c-126">SBA (survivable branch office) n’est pas pris en charge pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-126">SBA (survivable branch office) is not supported for XMPP.</span></span> <span data-ttu-id="f6f3c-127">Les utilisateurs hébergés dans des configurations SBA ne seront pas en mesure d’envoyer des messages instantanés ou de voir la présence de contacts XMPP.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-127">Users homed in a SBA configurations will not be able to send IMs or see Presence with XMPP contacts.</span></span>



<span data-ttu-id="f6f3c-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6f3c-128"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

