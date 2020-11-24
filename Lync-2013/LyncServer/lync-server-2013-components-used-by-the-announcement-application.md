---
title: 'Lync Server 2013 : Composants utilisés par l’application d’annonce'
description: 'Lync Server 2013 : composants utilisés par l’application d’annonce.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by the Announcement application
ms:assetid: 7b1a0281-cf31-459d-a734-5f10a129089c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398608(v=OCS.15)
ms:contentKeyID: 48184595
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5338ad097c814d5c6435bd89dbf7cfa8680feb8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394208"
---
# <a name="components-used-by-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="bdaf8-103">Composants utilisés par l’application d’annonce dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bdaf8-103">Components used by the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdaf8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdaf8-104">

<span> </span></span></span>

<span data-ttu-id="bdaf8-105">_**Dernière modification de la rubrique :** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="bdaf8-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="bdaf8-106">Dans Lync Server 2013, l’application d’annonce est un composant de l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-106">In Lync Server 2013, the Announcement application is a component of the Response Group application.</span></span> <span data-ttu-id="bdaf8-107">Lorsque vous déployez Enterprise Voice, l’application d’annonce est automatiquement installée et activée conjointement avec l’application Response Group.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-107">When you deploy Enterprise Voice, the Announcement application is automatically installed and activated along with the Response Group application.</span></span> <span data-ttu-id="bdaf8-108">Cette section décrit les composants qui prennent en charge l’application d’annonce.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-108">This section describes the components that support the Announcement application.</span></span>

<div>

## <a name="announcement-application-components"></a><span data-ttu-id="bdaf8-109">Composants de l’application annonce</span><span class="sxs-lookup"><span data-stu-id="bdaf8-109">Announcement Application Components</span></span>

<span data-ttu-id="bdaf8-110">Les composants Lync Server suivants prennent en charge l’application d’annonce :</span><span class="sxs-lookup"><span data-stu-id="bdaf8-110">The following Lync Server components support the Announcement application:</span></span>

  - <span data-ttu-id="bdaf8-111">**Service d’application**   Le service d’application fournit une plate-forme de déploiement, d’hébergement et de gestion des applications de communications unifiées.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-111">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications.</span></span> <span data-ttu-id="bdaf8-112">Le service d’application est automatiquement installé sur chaque serveur frontal d’une grappe frontale et sur tous les serveurs Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-112">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="bdaf8-113">**Application Response Group**   L’application Response Group est l’une des applications de communications unifiées hébergées par le service d’application.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-113">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="bdaf8-114">Lorsqu’une plage de numéros de téléphone non attribués est configurée pour diriger vers une annonce, l’application de groupe de réponse est requise pour acheminer les appels passés vers le numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-114">When an unassigned phone number range is configured to route to an announcement, the Response Group application is required to route the calls made to the phone number.</span></span> <span data-ttu-id="bdaf8-115">(L’application Response Group n’est pas nécessaire si toutes les plages sont configurées pour le routage à la messagerie unifiée Exchange (MU).)</span><span class="sxs-lookup"><span data-stu-id="bdaf8-115">(Response Group application is not required if all the ranges are configured to route to Exchange Unified Messaging (UM).)</span></span>

  - <span data-ttu-id="bdaf8-116">**Fichiers audio**   Les fichiers audio sont utilisés pour les annonces.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-116">**Audio files**   Audio files are used for the announcements.</span></span>

  - <span data-ttu-id="bdaf8-117">**Magasin de fichiers**   L’application d’annonce utilise le magasin de fichiers pour stocker ses fichiers audio.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-117">**File Store**   The Announcement application uses File Store to store its audio files.</span></span>

  - <span data-ttu-id="bdaf8-118">**Panneau de configuration de Lync Server**   Vous pouvez utiliser le panneau de configuration de Lync Server pour configurer la table des numéros non attribués.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-118">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the unassigned number table.</span></span>

  - <span data-ttu-id="bdaf8-119">**Lync Server Management Shell**   Vous pouvez utiliser les applets de cmdlet Lync Server Management Shell pour configurer les paramètres d’annonce et la table des numéros non attribués.</span><span class="sxs-lookup"><span data-stu-id="bdaf8-119">**Lync Server Management Shell**   You can use Lync Server Management Shell cmdlets to configure Announcement settings and the unassigned number table.</span></span>

<span data-ttu-id="bdaf8-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdaf8-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

