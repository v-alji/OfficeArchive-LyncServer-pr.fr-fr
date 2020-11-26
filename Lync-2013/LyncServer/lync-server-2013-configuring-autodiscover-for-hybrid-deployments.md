---
title: 'Lync Server 2013 : configuration de la découverte automatique pour les déploiements hybrides'
description: 'Lync Server 2013 : configuration de la découverte automatique pour les déploiements hybrides.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Autodiscover for hybrid deployments
ms:assetid: ca605e62-181c-42ca-80a1-e37e610f8277
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945653(v=OCS.15)
ms:contentKeyID: 51541521
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e6797e3f6b77e3016f6cef87f2a930f5a7c1fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433303"
---
# <a name="configuring-autodiscover-in-lync-server-2013-for-hybrid-deployments"></a><span data-ttu-id="fb6b2-103">Configuration de la découverte automatique dans Lync Server 2013 pour les déploiements hybrides</span><span class="sxs-lookup"><span data-stu-id="fb6b2-103">Configuring Autodiscover in Lync Server 2013 for hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb6b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb6b2-104">

<span> </span></span></span>

<span data-ttu-id="fb6b2-105">_**Dernière modification de la rubrique :** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="fb6b2-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="fb6b2-106">Les déploiements hybrides sont des configurations utilisant à la fois le service de Cloud Computing Microsoft Lync Online et le déploiement local.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-106">Hybrid Deployments are configurations that use both the Microsoft Lync Online cloud service and the on premises deployment.</span></span> <span data-ttu-id="fb6b2-107">Dans ce type de configuration, le service de découverte automatique doit être en mesure de localiser l’emplacement où l’utilisateur se trouve réellement.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-107">In this type of configuration, the Autodiscover service must be able to locate where the user is actually located.</span></span> <span data-ttu-id="fb6b2-108">Par exemple, la fonction de découverte automatique facilite la recherche du compte d’utilisateur et l’emplacement du serveur qui héberge le compte de l’utilisateur, même s’il se trouve dans le déploiement local ou dans le déploiement Lync Online.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-108">That is to say, Autodiscover aids in finding the user account and where the server that hosts the user’s account is, regardless if it is in the on premises deployment or in the Lync Online deployment.</span></span>

<span data-ttu-id="fb6b2-109">Par exemple, si le compte d’un utilisateur est hébergé sur un serveur dans Lync Online, la tentative de localisation de l’utilisateur se déroule comme suit, dans un processus connu sous le nom de *découverte*:</span><span class="sxs-lookup"><span data-stu-id="fb6b2-109">For example, if a user’s account is hosted on a server in Lync Online, the attempt to locate the user will happen as follows, in a process known as *discoverability*:</span></span>

  - <span data-ttu-id="fb6b2-110">Un utilisateur commence une tentative de connexion à un déploiement local, **contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-110">User initiates a connection attempt to the on premises deployment, **contoso.com**.</span></span>

  - <span data-ttu-id="fb6b2-111">La tentative est envoyée à lyncdiscover.contoso.com, le nom DNS associé au service de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-111">The attempt is sent to lyncdiscover.contoso.com, the DNS name associated with the Autodiscover service.</span></span>

  - <span data-ttu-id="fb6b2-112">La découverte automatique fait référence au pool d’inscriptions présumées au niveau du déploiement local de contoso.com et dispose d’informations sur le véritable serveur d’accueil hébergé dans Lync Online.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-112">Autodiscover refers to the assumed registrar pool at the contoso.com on premises deployment and is given information on the user’s actual home server hosted in Lync Online.</span></span> <span data-ttu-id="fb6b2-113">La découverte automatique envoie ensuite à l’utilisateur une référence au service de découverte automatique **Lync.com** online.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-113">Autodiscover then sends the user a referral to the **lync.com** online Autodiscover service.</span></span>

  - <span data-ttu-id="fb6b2-114">L’utilisateur entame une tentative de connexion au service de découverte automatique lync.com Online et est en mesure de trouver le compte de l’utilisateur et le serveur associé de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-114">The user initiates a connection attempt to the lync.com online Autodiscover service and is able to locate the user’s account and the user’s home server.</span></span>

<span data-ttu-id="fb6b2-115">Pour permettre aux clients de découvrir le déploiement sur lequel se trouve le serveur associé de l’utilisateur, vous devez configurer le service de découverte automatique à l’aide d’une nouvelle URL (Uniform Resource Locator).</span><span class="sxs-lookup"><span data-stu-id="fb6b2-115">To enable clients to discover the deployment where the user home server is located, you must configure the Autodiscover service with a new uniform resource locator (URL).</span></span> <span data-ttu-id="fb6b2-116">Procédez comme suit pour configurer le service de découverte automatique.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-116">Do the following to configure the Autodiscover service.</span></span>

<div>

## <a name="configuring-autodiscover-for-hybrid-deployments"></a><span data-ttu-id="fb6b2-117">Configuration de la découverte automatique pour les déploiements hybrides</span><span class="sxs-lookup"><span data-stu-id="fb6b2-117">Configuring Autodiscover for Hybrid Deployments</span></span>

1.  <span data-ttu-id="fb6b2-118">Dans la rubrique [Configuration requise pour le service de découverte automatique pour Lync Server 2013](lync-server-2013-autodiscover-service-requirements.md), vous utilisez Get-CsHostingProvider pour récupérer la valeur de l’attribut ProxyFQDN.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-118">In the topic, [Autodiscover service requirements for Lync Server 2013](lync-server-2013-autodiscover-service-requirements.md), you use Get-CsHostingProvider to retrieve the value of the attribute ProxyFQDN.</span></span>

2.  <span data-ttu-id="fb6b2-119">À partir de Lync Server Management Shell, tapez</span><span class="sxs-lookup"><span data-stu-id="fb6b2-119">From the Lync Server Management Shell, type</span></span>
    
        Set-CsHostingProvider -Identity [identity] -AutodiscoverUrl https://webdir.online.lync.com/autodiscover/autodisccoverservice.svc/root
    
    <span data-ttu-id="fb6b2-120">Où \[ Identity \] est remplacé par le nom de domaine de l’espace d’adressage SIP partagé.</span><span class="sxs-lookup"><span data-stu-id="fb6b2-120">Where \[identity\] is replaced with the domain name of the shared SIP address space.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fb6b2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb6b2-121">See Also</span></span>


[<span data-ttu-id="fb6b2-122">Get-CsHostingProvider</span><span class="sxs-lookup"><span data-stu-id="fb6b2-122">Get-CsHostingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostingProvider)  
[<span data-ttu-id="fb6b2-123">Set-CsHostingProvider</span><span class="sxs-lookup"><span data-stu-id="fb6b2-123">Set-CsHostingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostingProvider)  
  

<span data-ttu-id="fb6b2-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb6b2-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

