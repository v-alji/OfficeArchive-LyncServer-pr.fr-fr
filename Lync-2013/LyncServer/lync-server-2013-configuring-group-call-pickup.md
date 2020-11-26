---
title: 'Lync Server 2013 : configuration de la cueillette des appels de groupe'
description: 'Lync Server 2013 : configuration de la cueillette d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Group Call Pickup
ms:assetid: b4b0a9a0-91c6-43a5-9e2b-a086caeb3f94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945645(v=OCS.15)
ms:contentKeyID: 51541505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff6be1ea20a98cfaf2addf32c7767940b420c5c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433030"
---
# <a name="configuring-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="67851-103">Configuration de la collecte d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-103">Configuring Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67851-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67851-104">

<span> </span></span></span>

<span data-ttu-id="67851-105">_**Dernière modification de la rubrique :** 2013-02-01_</span><span class="sxs-lookup"><span data-stu-id="67851-105">_**Topic Last Modified:** 2013-02-01_</span></span>

<span data-ttu-id="67851-106">Mise à jour cumulative pour Lync Server 2013 : février 2013 présente la capture d’appel de groupe comme nouvelle fonctionnalité voix entreprise.</span><span class="sxs-lookup"><span data-stu-id="67851-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="67851-107">La cueillette de groupe permet aux utilisateurs de décrocher les appels qui sonnent pour un autre utilisateur en composant un numéro de groupe de capture d’appel.</span><span class="sxs-lookup"><span data-stu-id="67851-107">Group Call Pickup lets users pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="67851-108">Les composants utilisés par le biais du groupe de collecte d’appels sont automatiquement installés et activés sur le serveur frontal ou le serveur Standard Edition lors du déploiement d’Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="67851-108">The components that Group Call Pickup uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="67851-109">Toutefois, vous devez configurer la cueillette d’appel de groupe avant qu’elle ne soit disponible pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="67851-109">However, you must configure Group Call Pickup before it is available to users.</span></span>

<span data-ttu-id="67851-110">Cette section vous guide dans la configuration de la sélection d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="67851-110">This section guides you through the configuration of Group Call Pickup.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67851-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="67851-111">In This Section</span></span>

[<span data-ttu-id="67851-112">Configuration requise pour les appels de groupe et droits d’utilisateur dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-112">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-group-call-pickup-configuration-prerequisites-and-user-rights.md)

[<span data-ttu-id="67851-113">Processus de déploiement pour l’enlèvement de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-113">Deployment process for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-group-call-pickup.md)

[<span data-ttu-id="67851-114">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-114">Deploy the SEFAUtil tool in Lync Server 2013</span></span>](lync-server-2013-deploy-the-sefautil-tool.md)

[<span data-ttu-id="67851-115">Configurer des numéros de groupe de capture d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-115">Configure call pickup group numbers in Lync Server 2013</span></span>](lync-server-2013-configure-call-pickup-group-numbers.md)

[<span data-ttu-id="67851-116">Activer le prélèvement d’appels de groupe pour les utilisateurs dans Lync Server 2013 et affecter un numéro de groupe</span><span class="sxs-lookup"><span data-stu-id="67851-116">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>](lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md)

[<span data-ttu-id="67851-117">Communiquer des attributions d’appels de groupe aux utilisateurs dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-117">Communicate Group Call Pickup assignments to users in Lync Server 2013</span></span>](lync-server-2013-communicate-group-call-pickup-assignment-to-users.md)

[<span data-ttu-id="67851-118">Facultatif Vérifier le déploiement d’un appel de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67851-118">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-the-group-call-pickup-deployment.md)

<span data-ttu-id="67851-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67851-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

