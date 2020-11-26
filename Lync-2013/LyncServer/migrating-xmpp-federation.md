---
title: Migration de la fédération XMPP
description: Migration de la Fédération XMPP.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440359"
---
# <a name="migrating-xmpp-federation"></a><span data-ttu-id="54e91-103">Migration de la fédération XMPP</span><span class="sxs-lookup"><span data-stu-id="54e91-103">Migrating XMPP federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54e91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54e91-104">

<span> </span></span></span>

<span data-ttu-id="54e91-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="54e91-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="54e91-106">Les versions précédentes de Lync Server et d’Office Communications Server ont fourni une passerelle XMPP (extensible Messaging and Presence Protocol) qui pouvait être déployée en tant que rôle de serveur distinct pour permettre la Fédération avec des déploiements de XMPP.</span><span class="sxs-lookup"><span data-stu-id="54e91-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="54e91-107">Dans Lync Server 2013, la fonctionnalité XMPP peut être déployée en tant que fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="54e91-107">In Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="54e91-108">La fonctionnalité XMPP est installée en deux parties : en tant que proxy XMPP qui s’exécute sur le serveur Edge Lync Server 2013 et la passerelle XMPP qui s’exécute sur le serveur frontal 2013 Lync Server.</span><span class="sxs-lookup"><span data-stu-id="54e91-108">XMPP functionality is installed in two parts: as an XMPP proxy that runs on the Lync Server 2013 Edge Server, and the XMPP Gateway that runs on the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="54e91-109">Du point de vue de la migration, vous pouvez déplacer un compte d’utilisateur Lync Server vers un pool Lync Server 2013 et continuer à utiliser la passerelle XMPP héritée.</span><span class="sxs-lookup"><span data-stu-id="54e91-109">From a migration perspective, a Lync Server user account can be moved to a Lync Server 2013 pool and continue to use the legacy XMPP gateway.</span></span> <span data-ttu-id="54e91-110">Ce n’est possible que lorsque le partenaire fédéré de XMPP n’est pas configuré dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54e91-110">This is possible only when the XMPP federated partner is not configured in Lync Server 2013.</span></span>

<span data-ttu-id="54e91-111">En résumé, si Lync Server 2010 a été déployé à l’aide d’Office Communications Server 2007 R2 XMPP Gateway et XMPP Federation pour les utilisateurs hérités de Lync Server 2010, vous pouvez migrer la Fédération XMPP vers Lync Server 2013 :</span><span class="sxs-lookup"><span data-stu-id="54e91-111">In summary, if Lync Server 2010 has been deployed with the Office Communications Server 2007 R2 XMPP Gateway and XMPP federation has been enabled for legacy Lync Server 2010 users, to migrate the XMPP federation to Lync Server 2013:</span></span>

1.  <span data-ttu-id="54e91-112">Déploiement d’un pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54e91-112">Deploy a Lync Server 2013 pool.</span></span>

2.  <span data-ttu-id="54e91-113">Déploiement d’un serveur Edge Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54e91-113">Deploy a Lync Server 2013 Edge server.</span></span>

3.  <span data-ttu-id="54e91-114">Déplacer tous les utilisateurs vers le pool Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54e91-114">Move all users to the Lync Server 2013 pool</span></span>

4.  <span data-ttu-id="54e91-115">Créez des stratégies d’accès XMPP et des certificats pour le serveur de périphérie.</span><span class="sxs-lookup"><span data-stu-id="54e91-115">Create XMPP access policies and certificates for the Edge Server.</span></span>

5.  <span data-ttu-id="54e91-116">Activez la Fédération XMPP dans Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54e91-116">Enable XMPP federation in Lync Server 2013.</span></span> 

6.  <span data-ttu-id="54e91-117">Mettez à jour les entrées DNS de façon à ce qu’elle pointe vers la passerelle XMPP Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="54e91-117">Update the DNS entries to point to the Lync Server 2013 XMPP Gateway.</span></span>

<span data-ttu-id="54e91-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54e91-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

