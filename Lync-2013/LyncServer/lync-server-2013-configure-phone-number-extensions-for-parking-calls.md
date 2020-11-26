---
title: 'Lync Server 2013 : configurer les extensions de numéro de téléphone pour les appels en stationnement'
description: 'Lync Server 2013 : configurer les extensions de numéro de téléphone pour les appels en stationnement.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure phone number extensions for parking calls
ms:assetid: fbf97624-9587-42a6-b276-1b69c574a74d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182611(v=OCS.15)
ms:contentKeyID: 48185980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6219e04243d0c19bc37251f7d113f7ebdd09fb72
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433807"
---
# <a name="configure-phone-number-extensions-for-parking-calls-in-lync-server-2013"></a><span data-ttu-id="e62b8-103">Configurer les extensions de numéro de téléphone pour les appels de parking dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e62b8-103">Configure phone number extensions for parking calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e62b8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e62b8-104">

<span> </span></span></span>

<span data-ttu-id="e62b8-105">_**Dernière modification de la rubrique :** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="e62b8-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="e62b8-106">L’application de parc d’appels utilise des numéros d’extension dans la table de parc d’appels pour les appels de parc.</span><span class="sxs-lookup"><span data-stu-id="e62b8-106">The Call Park application uses extension numbers in the Call Park orbit table to park calls.</span></span> <span data-ttu-id="e62b8-107">Vous devez configurer la table d’orbite du parc d’appels avec les plages de numéros d’extension que votre organisation réserve pour les appels en stationnement.</span><span class="sxs-lookup"><span data-stu-id="e62b8-107">You need to configure the Call Park orbit table with the ranges of extension numbers that your organization reserves for parked calls.</span></span> <span data-ttu-id="e62b8-108">Ces postes doivent être des postes virtuels (autrement dit, des postes auxquels aucun utilisateur ni téléphone n’est affecté).</span><span class="sxs-lookup"><span data-stu-id="e62b8-108">These extensions need to be virtual extensions (that is, extensions that have no user or phone assigned to them).</span></span> <span data-ttu-id="e62b8-109">Chaque pool de serveurs Lync dans lequel une application de parc d’appels est déployée et configurée peut avoir une ou plusieurs plages d’orbite.</span><span class="sxs-lookup"><span data-stu-id="e62b8-109">Each Lync Server pool where a Call Park application is deployed and configured can have one or more orbit ranges.</span></span> <span data-ttu-id="e62b8-110">Les plages orbites doivent être globalement uniques dans le déploiement de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e62b8-110">Orbit ranges must be globally unique across the Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="e62b8-111">Vous devez activer la case à cocher <STRONG>activer le parc d’appels</STRONG> dans votre politique vocale pour pouvoir utiliser le parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="e62b8-111">You must select the <STRONG>Enable call park</STRONG> check box in your voice policy before you can use Call Park.</span></span> <span data-ttu-id="e62b8-112">Par défaut, cette option n’est pas sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e62b8-112">By default, this option is not selected.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e62b8-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e62b8-113">In This Section</span></span>

  - [<span data-ttu-id="e62b8-114">Créer ou modifier une gamme de parc d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e62b8-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

  - [<span data-ttu-id="e62b8-115">Supprimer une gamme de stationnement d’appels dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e62b8-115">Delete a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-delete-a-call-park-orbit-range.md)

<span data-ttu-id="e62b8-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e62b8-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

