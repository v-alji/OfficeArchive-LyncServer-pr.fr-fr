---
title: 'Lync Server 2013 : hybride et fractionné-domaine-découverte automatique'
description: 'Lync Server 2013 : hybride et fractionné-domaine-découverte automatique.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hybrid and split-domain - Autodiscover
ms:assetid: c855bcc5-b656-4d2d-92d6-f016f2797d3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945652(v=OCS.15)
ms:contentKeyID: 51541520
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 972233fd10d2b68a002d2d3a203f61bb0bd29574
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427438"
---
# <a name="hybrid-and-split-domain---autodiscover-in-lync-server-2013"></a><span data-ttu-id="01116-103">Domaines hybrides et fractionnés-découverte automatique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01116-103">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01116-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01116-104">

<span> </span></span></span>

<span data-ttu-id="01116-105">_**Dernière modification de la rubrique :** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="01116-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="01116-106">Un espace d’adressage SIP partagé, également connu sous le nom de déploiement *Split-Domain* ou d’un déploiement *hybride* , est une configuration dans laquelle les utilisateurs sont déployés dans un déploiement local et un environnement en ligne.</span><span class="sxs-lookup"><span data-stu-id="01116-106">A shared SIP address space, also known as a *split-domain* deployment, or a *hybrid* deployment, is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="01116-107">Le résultat escompté est d’avoir un utilisateur, où qu’il se trouve (en local ou en ligne), de se connecter au déploiement et d’être redirigé vers son emplacement du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="01116-107">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="01116-108">Pour ce faire, la fonctionnalité de découverte automatique de Lync Server 2013 est utilisée pour rediriger l’utilisateur en ligne vers la topologie en ligne.</span><span class="sxs-lookup"><span data-stu-id="01116-108">To accomplish this, the Autodiscover feature of Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="01116-109">Pour ce faire, vous pouvez configurer le localisateur de ressources uniformes de découverte automatique (URL) à l’aide de Lync Server Management Shell, de l’applet **de action Get-CsHostingProvider** et de l’applet **de passe Set-CsHostingProvider** .</span><span class="sxs-lookup"><span data-stu-id="01116-109">You can do this by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell, the **Get-CsHostingProvider** cmdlet, and the **Set-CsHostingProvider** cmdlet.</span></span>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="01116-110">Mobilité pour le déploiement de domaines fractionnés</span><span class="sxs-lookup"><span data-stu-id="01116-110">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="01116-111">Vous devrez collecter et enregistrer les attributs déployés suivants :</span><span class="sxs-lookup"><span data-stu-id="01116-111">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="01116-112">À partir de Lync Server Management Shell, tapez</span><span class="sxs-lookup"><span data-stu-id="01116-112">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="01116-113">Dans les résultats, recherchez le fournisseur en ligne doté de l’attribut **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="01116-113">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="01116-114">Par exemple, sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="01116-114">For example, sipfed.online.lync.com.</span></span>

  - <span data-ttu-id="01116-115">Enregistrez la valeur de ProxyFQDN.</span><span class="sxs-lookup"><span data-stu-id="01116-115">Record the value of the ProxyFQDN.</span></span>

  - <span data-ttu-id="01116-116">Activez la Fédération sur le panneau de configuration de Lync Server sur site, en autorisant la Fédération avec le fournisseur en ligne.</span><span class="sxs-lookup"><span data-stu-id="01116-116">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider.</span></span>

  - <span data-ttu-id="01116-117">Activez la Fédération pour le fournisseur en ligne.</span><span class="sxs-lookup"><span data-stu-id="01116-117">Enable federation for the online provider.</span></span> <span data-ttu-id="01116-118">Par défaut, tous les utilisateurs en ligne sont activés pour la Fédération de domaine et peuvent communiquer avec tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="01116-118">By default, all online users are enabled for domain federation and can communicate with all domains.</span></span>

  - <span data-ttu-id="01116-119">Si vous définissez des domaines bloqués et autorisés, déterminez les domaines à autoriser ou bloquer explicitement.</span><span class="sxs-lookup"><span data-stu-id="01116-119">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block.</span></span>

  - <span data-ttu-id="01116-120">Pour la Fédération en ligne, vous devez prévoir des exceptions de pare-feu, des certificats et l’hôte DNS (A ou AAAA, si vous utilisez des enregistrements IPv6).</span><span class="sxs-lookup"><span data-stu-id="01116-120">For online federation, you must plan for firewall exceptions, certificates, and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="01116-121">Par ailleurs, vous devez configurer des stratégies de Fédération.</span><span class="sxs-lookup"><span data-stu-id="01116-121">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="01116-122">Pour plus d’informations, reportez-vous [à planification de Lync server 2013 et la Fédération Office Communications Server](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span><span class="sxs-lookup"><span data-stu-id="01116-122">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span></span>

<span data-ttu-id="01116-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01116-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

