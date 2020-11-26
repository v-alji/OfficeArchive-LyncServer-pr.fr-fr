---
title: 'Lync Server 2013 : Configuration du directeur'
description: 'Lync Server 2013 : configuration du Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up the Director
ms:assetid: 408b76f7-6fdd-4e50-8a3e-e87db12c1394
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425915(v=OCS.15)
ms:contentKeyID: 48183951
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b917000dec6d30fdec2963ff1e464fbb9a70805
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423903"
---
# <a name="setting-up-the-director-in-lync-server-2013"></a><span data-ttu-id="d67b9-103">Configuration du directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-103">Setting up the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d67b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d67b9-104">

<span> </span></span></span>

<span data-ttu-id="d67b9-105">_**Dernière modification de la rubrique :** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="d67b9-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="d67b9-106">Si vous autorisez l’accès pour les utilisateurs externes en déployant des serveurs Edge, il est possible de déployer un réalisateur.</span><span class="sxs-lookup"><span data-stu-id="d67b9-106">If you’re enabling access for external users by deploying Edge Servers, one option is to deploy a Director.</span></span> <span data-ttu-id="d67b9-107">Un directeur est un serveur exécutant Microsoft Lync Server 2013 qui authentifie les demandes des utilisateurs, mais ne possède pas de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d67b9-107">A Director is a server running Microsoft Lync Server 2013 that authenticates user requests, but doesn’t home any user accounts.</span></span> <span data-ttu-id="d67b9-108">Ce n’est pas une condition requise, mais elle est très utile si vous avez des problèmes de performances et souhaitez rationaliser les demandes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d67b9-108">Now, this isn’t a requirement, but it is very helpful if you’re worried about performance and want to help streamline authentication requests.</span></span> <span data-ttu-id="d67b9-109">Si vous décidez qu’il s’agit d’une bonne idée de votre organisation, les étapes de configuration d’un directeur ou d’un pool de réalisateurs sont similaires à la configuration d’un pool d’entreprise frontal Enterprise Edition ou d’un serveur Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="d67b9-109">If you decide this is a good idea for your organization, the steps to set up a Director or a Director pool are similar to setting up either an Enterprise Edition Front End pool or Standard Edition server.</span></span> <span data-ttu-id="d67b9-110">Après avoir défini votre ou vos réalisateurs dans le générateur de topologie, vous devez effectuer les étapes décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="d67b9-110">After you’ve defined your Director(s) in Topology Builder, you’ll need to perform the steps in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d67b9-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d67b9-111">In This Section</span></span>

  - [<span data-ttu-id="d67b9-112">Installation du magasin de configurations local dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-112">Install the Local Configuration store in Lync Server 2013</span></span>](lync-server-2013-install-the-local-configuration-store.md)

  - [<span data-ttu-id="d67b9-113">Installation de Lync Server 2013 sur le directeur</span><span class="sxs-lookup"><span data-stu-id="d67b9-113">Install Lync Server 2013 on the Director</span></span>](lync-server-2013-install-lync-server-on-the-director.md)

  - [<span data-ttu-id="d67b9-114">Configuration des certificats pour le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-114">Configure certificates for the Director in Lync Server 2013</span></span>](lync-server-2013-configure-certificates-for-the-director.md)

  - [<span data-ttu-id="d67b9-115">Démarrage des services sur le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-115">Start services on the Director in Lync Server 2013</span></span>](lync-server-2013-start-services-on-the-director.md)

  - [<span data-ttu-id="d67b9-116">Test du directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-116">Test the Director in Lync Server 2013</span></span>](lync-server-2013-test-the-director.md)

  - [<span data-ttu-id="d67b9-117">Configuration de la connexion automatique du client pour utiliser le directeur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d67b9-117">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>](lync-server-2013-configure-automatic-client-sign-in-to-use-the-director.md)

<span data-ttu-id="d67b9-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d67b9-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

