---
title: 'Lync Server 2013 : composants utilisés par le prélèvement d’appels de groupe'
description: 'Lync Server 2013 : composants utilisés par le prélèvement d’appels de groupe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394209"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="ce2bb-103">Composants utilisés par le prélèvement d’appels de groupe dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce2bb-103">Components used by Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce2bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce2bb-104">

<span> </span></span></span>

<span data-ttu-id="ce2bb-105">_**Dernière modification de la rubrique :** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="ce2bb-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="ce2bb-106">La prise d’appel de groupe est déployée automatiquement lors du déploiement de l’application voix entreprise et de l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-106">Group Call Pickup is automatically deployed when you deploy Enterprise Voice and the Call Park application.</span></span> <span data-ttu-id="ce2bb-107">Vous pouvez activer le prélèvement d’appels de groupe en configurant la table orbite du parc d’appels avec des plages de numéros distinctes désignés comme numéros de groupe de capture d’appel, puis en attribuant aux utilisateurs la possibilité d’appeler les groupes de capture et en permettant aux utilisateurs de procéder à un appel de groupe.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-107">You enable Group Call Pickup by configuring the Call Park orbit table with separate ranges of numbers designated as call pickup group numbers, and then by assigning users to call pickup groups and enabling the users for Group Call Pickup.</span></span> <span data-ttu-id="ce2bb-108">Les composants Lync Server suivants prennent en charge la cueillette des appels de groupe :</span><span class="sxs-lookup"><span data-stu-id="ce2bb-108">The following Lync Server components support Group Call Pickup:</span></span>

  - <span data-ttu-id="ce2bb-109">**Service d’application**   Le service d’application fournit une plateforme de déploiement, d’hébergement et de gestion d’applications de communications unifiées, telles que l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="ce2bb-110">Le service d’application est automatiquement installé sur chaque serveur frontal d’une grappe frontale et sur tous les serveurs Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="ce2bb-111">**Application de parc d’appels**   L’application de parc d’appels est l’une des applications de communications unifiées hébergées par le service d’application.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="ce2bb-112">Le prélèvement d’appels de groupe est basé sur l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-112">Group Call Pickup is based on the Call Park application.</span></span>

  - <span data-ttu-id="ce2bb-113">**Lync Server Management Shell**   Vous utilisez Lync Server Management Shell pour gérer les groupes de capture d’appels de groupe.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-113">**Lync Server Management Shell**   You use Lync Server Management Shell to manage Group Call Pickup groups.</span></span>

  - <span data-ttu-id="ce2bb-114">**Outil du kit de ressources SEFAUtil**   Vous pouvez utiliser l’utilitaire d’activation de fonctionnalité d’extension secondaire (SEFAUtil) pour attribuer des utilisateurs à un groupe de capture d’appel et activer ou désactiver le prélèvement d’appels pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-114">**SEFAUtil resource kit tool**   You use the secondary extension feature activation utility (SEFAUtil) to assign users to a call pickup group and to enable or disable call pickup for users.</span></span>

<span data-ttu-id="ce2bb-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce2bb-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

