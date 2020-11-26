---
title: 'Lync Server 2013 : Configuration du parcage d’appel'
description: 'Lync Server 2013 : configuration du parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Call Park
ms:assetid: e4c5da53-7f6c-4535-bc9b-9da2026caec8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399014(v=OCS.15)
ms:contentKeyID: 48185732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2708f26fae5706afc31aa195b9fdb82536247b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433247"
---
# <a name="configuring-call-park-in-lync-server-2013"></a><span data-ttu-id="1dc1a-103">Configuration du parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-103">Configuring Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1dc1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1dc1a-104">

<span> </span></span></span>

<span data-ttu-id="1dc1a-105">_**Dernière modification de la rubrique :** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="1dc1a-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="1dc1a-106">Le parc d’appels permet à un utilisateur d’entreprise Voice de mettre un appel en attente d’un seul téléphone, puis de récupérer l’appel ultérieurement en composant un numéro interne (connu sous le nom de bobine *de parking)* depuis n’importe quel téléphone.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-106">Call Park enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later by dialing an internal number (known as a Call Park *orbit*) from any telephone.</span></span>

<span data-ttu-id="1dc1a-107">Les composants utilisés par le parc d’appels sont automatiquement installés et activés sur le serveur frontal ou le serveur Standard Edition lors du déploiement d’Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-107">The components that Call Park uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="1dc1a-108">Toutefois, vous devez configurer le parc d’appels avant qu’il soit disponible pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-108">However, you must configure Call Park before it is available to users.</span></span>

<span data-ttu-id="1dc1a-109">Cette section vous guide dans la configuration du parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-109">This section guides you through the configuration of Call Park.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1dc1a-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1dc1a-110">In This Section</span></span>

  - [<span data-ttu-id="1dc1a-111">Conditions prérequises pour la configuration du parcage d’appel et des droits utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-111">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-call-park-configuration-prerequisites-and-user-rights.md)

  - [<span data-ttu-id="1dc1a-112">Processus de déploiement du parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-112">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="1dc1a-113">Configuration de la table d’orbites de parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-113">Configure the Call Park orbit table in Lync Server 2013</span></span>](lync-server-2013-configure-the-call-park-orbit-table.md)

  - [<span data-ttu-id="1dc1a-114">Configurer les paramètres de parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-114">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="1dc1a-115">Personnaliser le parc d’appels en attente dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-115">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="1dc1a-116">Activer le parc d’appels pour les utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-116">Enable Call Park for users in Lync Server 2013</span></span>](lync-server-2013-enable-call-park-for-users.md)

  - [<span data-ttu-id="1dc1a-117">Vérifier les règles de normalisation du parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-117">Verify normalization rules for Call Park in Lync Server 2013</span></span>](lync-server-2013-verify-normalization-rules-for-call-park.md)

  - [<span data-ttu-id="1dc1a-118">Facultatif Vérifier le déploiement du parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dc1a-118">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-call-park-deployment.md)

<span data-ttu-id="1dc1a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1dc1a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

