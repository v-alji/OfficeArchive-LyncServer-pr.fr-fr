---
title: Scénario de migration standard - Haut niveau
description: Scénario de migration standard-niveau supérieur.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Standard migration scenario - high-level
ms:assetid: e768a7ca-44e3-4969-a6d9-7ed3e7029c5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205354(v=OCS.15)
ms:contentKeyID: 48185709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a931b76e528b7e6468f6b7e7b9a718724d27501f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438756"
---
# <a name="standard-migration-scenario---high-level"></a><span data-ttu-id="043e7-103">Scénario de migration standard - Haut niveau</span><span class="sxs-lookup"><span data-stu-id="043e7-103">Standard migration scenario - high-level</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="043e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="043e7-104">

<span> </span></span></span>

<span data-ttu-id="043e7-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="043e7-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="043e7-106">Utilisez les éléments suivants comme point de départ lors de la migration de Lync Server 2010, d’une conversation de groupe ou d’une conversation de groupe Office Communications Server 2007 R2 vers Lync Server 2013, serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="043e7-106">Use the following items as a starting point when migrating Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="043e7-107">Le chemin de migration standard de Lync Server 2013 est le suivant :</span><span class="sxs-lookup"><span data-stu-id="043e7-107">The standard Lync Server 2013 migration path is as follows:</span></span>

  - <span data-ttu-id="043e7-108">Votre organisation a déjà déployé Lync Server 2010, les discussions de groupe ou les discussions de groupe Office Communications Server 2007 R2 et vous voulez déployer Lync Server 2013, serveur de conversation permanent.</span><span class="sxs-lookup"><span data-stu-id="043e7-108">Your organization has previously deployed Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat, and you want to deploy Lync Server 2013, Persistent Chat Server.</span></span>

  - <span data-ttu-id="043e7-109">Déploiement de Lync Server 2013, puis déploiement du ou des pools de serveurs de chat permanents.</span><span class="sxs-lookup"><span data-stu-id="043e7-109">Deploy Lync Server 2013, and then deploy Persistent Chat Server pool(s).</span></span>

  - <span data-ttu-id="043e7-110">Préparez et planifiez la migration de vos salles de conversation permanente et déterminez un moment approprié pour arrêter le système à des fins de migration.</span><span class="sxs-lookup"><span data-stu-id="043e7-110">Prepare and plan for migration of your Persistent Chat rooms, and determine an appropriate time to shut down the system for migration.</span></span>

  - <span data-ttu-id="043e7-111">Exécutez les cmdlets Windows PowerShell pour la migration (**Export-CsPersistentChatData** et **Import-CsPersistentChatData**) pour déplacer le contenu vers le serveur de conversation persistante.</span><span class="sxs-lookup"><span data-stu-id="043e7-111">Run the Windows PowerShell cmdlets for migration (**Export-CsPersistentChatData** and **Import-CsPersistentChatData**) to move content to Persistent Chat Server.</span></span>

  - <span data-ttu-id="043e7-112">Vérifiez que la migration a réussi.</span><span class="sxs-lookup"><span data-stu-id="043e7-112">Verify that migration has succeeded.</span></span>

  - <span data-ttu-id="043e7-113">Désaffectez votre déploiement hérité.</span><span class="sxs-lookup"><span data-stu-id="043e7-113">Decommission your legacy deployment.</span></span>

  - <span data-ttu-id="043e7-114">Configurez le serveur de chat permanent de sorte que les clients hérités puissent se connecter à Lync Server 2013, serveur de chat permanent.</span><span class="sxs-lookup"><span data-stu-id="043e7-114">Configure Persistent Chat Server so that legacy clients can connect to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="043e7-115">Cela est nécessaire, car cela prend du temps pour le déploiement de nouveaux clients, et vous voulez permettre aux utilisateurs existants d’avoir accès à leurs salles de conversation le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="043e7-115">This is necessary because it takes time to deploy new clients, and you want to enable existing users with legacy clients to have access to their chat rooms as soon as possible.</span></span>

  - <span data-ttu-id="043e7-116">Déployez de nouveaux clients tout en continuant de garantir que les travailleurs disposant d’une discussion de groupe héritée (clients) pourront accéder à leurs salles de conversation.</span><span class="sxs-lookup"><span data-stu-id="043e7-116">Deploy new clients, while continuing to help ensure that workers with legacy Group Chat (clients) can get to their chat rooms.</span></span>

<span data-ttu-id="043e7-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="043e7-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

