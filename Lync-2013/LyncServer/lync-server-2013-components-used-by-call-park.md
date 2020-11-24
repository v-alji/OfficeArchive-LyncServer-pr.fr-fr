---
title: 'Lync Server 2013 : Composants utilisés par le parcage d’appel'
description: 'Lync Server 2013 : composants utilisés par le parc d’appels.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394212"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="13a88-103">Composants utilisés par le parcage d’appel dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="13a88-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="13a88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="13a88-104">

<span> </span></span></span>

<span data-ttu-id="13a88-105">_**Dernière modification de la rubrique :** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="13a88-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="13a88-106">L’application de parc d’appels est automatiquement installée lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="13a88-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="13a88-107">Vous pouvez activer le parc d’appels en configurant une politique vocale.</span><span class="sxs-lookup"><span data-stu-id="13a88-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="13a88-108">Les composants Lync Server 2013 suivants prennent en charge l’application de stationnement d’appel :</span><span class="sxs-lookup"><span data-stu-id="13a88-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="13a88-109">**Service d’application**   Le service d’application fournit une plateforme de déploiement, d’hébergement et de gestion d’applications de communications unifiées, telles que l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="13a88-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="13a88-110">Le service d’application est automatiquement installé sur chaque serveur frontal d’une grappe frontale et sur tous les serveurs Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="13a88-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="13a88-111">**Application de parc d’appels**   L’application de parc d’appels est l’une des applications de communications unifiées hébergées par le service d’application.</span><span class="sxs-lookup"><span data-stu-id="13a88-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="13a88-112">Elle est incluse automatiquement lorsque vous déployez Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="13a88-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="13a88-113">Le parc d’appels de parc et de parking et de stationnement d’appels.</span><span class="sxs-lookup"><span data-stu-id="13a88-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="13a88-114">**Musique en attente-fichier**   Si la musique est activée, le fichier de musique est lu lors du stationnement d’un appel.</span><span class="sxs-lookup"><span data-stu-id="13a88-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="13a88-115">Un fichier de musique par défaut est inclus lors de l’installation de l’application de parc d’appels.</span><span class="sxs-lookup"><span data-stu-id="13a88-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="13a88-116">**Magasin de fichiers**   L’application de parc d’appels utilise le magasin de fichiers pour contenir des fichiers audio personnalisés.</span><span class="sxs-lookup"><span data-stu-id="13a88-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="13a88-117">**Panneau de configuration de Lync Server**   Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer la table d’orbite du parc d’appels et activer le parc d’appels pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="13a88-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="13a88-118">**Lync Server Management Shell**   Toutes les configurations d’application de parc d’appels peuvent être effectuées à l’aide des applets de applet Lync Server Management Shell.</span><span class="sxs-lookup"><span data-stu-id="13a88-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="13a88-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="13a88-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

