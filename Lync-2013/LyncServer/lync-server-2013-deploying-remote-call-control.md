---
title: 'Lync Server 2013 : Déploiement du contrôle d’appel distant'
description: 'Lync Server 2013 : déploiement du contrôle d’appel distant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying remote call control
ms:assetid: 763037f7-7a2a-49ae-acc3-9781b0bff7e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558664(v=OCS.15)
ms:contentKeyID: 48184536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc5e79f3ee44c354baf435585d304574d6a980c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429782"
---
# <a name="deploying-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="ebf88-103">Déploiement du contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-103">Deploying remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ebf88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ebf88-104">

<span> </span></span></span>

<span data-ttu-id="ebf88-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="ebf88-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="ebf88-106">Cette section vous guide tout au long du processus de déploiement de la fonctionnalité de contrôle d’appel distant pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ebf88-106">This section guides you through the process of deploying remote call control functionality to users in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ebf88-107">Bien que les fonctionnalités de contrôle d’appel distant soient accessibles aux utilisateurs distants alors qu’ils ne sont pas en dehors du pare-feu de votre organisation, les détails sur le déploiement de scénarios d’accès externes ne sont pas abordés dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="ebf88-107">Although remote call control features are available to remote users while they are outside of your organization’s firewall, details about deploying external access scenarios are beyond the scope of this documentation.</span></span> <span data-ttu-id="ebf88-108">Pour plus d’informations sur le déploiement d’un accès utilisateur externe, voir <A href="lync-server-2013-deploying-external-user-access.md">déploiement d’un accès utilisateur externe dans Lync Server 2013</A> dans la documentation de déploiement.</span><span class="sxs-lookup"><span data-stu-id="ebf88-108">For details about deploying external user access, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ebf88-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ebf88-109">In This Section</span></span>

  - [<span data-ttu-id="ebf88-110">Configuration de Lync Server 2013 pour le routage vers une passerelle SIP/CSTA</span><span class="sxs-lookup"><span data-stu-id="ebf88-110">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>](lync-server-2013-configuring-lync-server-to-route-to-a-sip-csta-gateway.md)

  - [<span data-ttu-id="ebf88-111">Configuration d’un itinéraire statique pour le contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-111">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="ebf88-112">Configuration d’une entrée d’application approuvée pour le contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-112">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

  - <span data-ttu-id="ebf88-113">[Définition d’une adresse IP de passerelle SIP/CSTA dans Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (uniquement si la passerelle est configurée pour utiliser TCP)</span><span class="sxs-lookup"><span data-stu-id="ebf88-113">[Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (only if the gateway is configured to use TCP)</span></span>

  - [<span data-ttu-id="ebf88-114">Activation des utilisateurs Lync pour le contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-114">Enable Lync users for remote call control in Lync Server 2013</span></span>](lync-server-2013-enable-lync-users-for-remote-call-control.md)

  - [<span data-ttu-id="ebf88-115">Contrôle d’appel distant et normalisation des numéros de téléphone dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-115">Remote call control and phone number normalization in Lync Server 2013</span></span>](lync-server-2013-remote-call-control-and-phone-number-normalization.md)

  - <span data-ttu-id="ebf88-116">[Supprimer un hôte autorisé hérité de Lync Server 2013 (facultatif)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (uniquement si vous migrez des utilisateurs déjà activés pour le contrôle d’appel distant)</span><span class="sxs-lookup"><span data-stu-id="ebf88-116">[Remove a legacy authorized host in Lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (only if you are migrating users previously enabled for remote call control)</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="ebf88-117">Sections associées</span><span class="sxs-lookup"><span data-stu-id="ebf88-117">Related Sections</span></span>

[<span data-ttu-id="ebf88-118">Planification du contrôle d’appel distant dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ebf88-118">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

<span data-ttu-id="ebf88-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ebf88-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

