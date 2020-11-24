---
title: 'Lync Server 2013 : configuration d’un emplacement de sauvegarde'
description: 'Lync Server 2013 : configuration d’un emplacement de sauvegarde'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up a backup location
ms:assetid: 006732eb-3d44-414d-8010-227a855caa93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202158(v=OCS.15)
ms:contentKeyID: 51541440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 344baea1b7e51454bb28d31d88451d29fd6aa3a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394961"
---
# <a name="setting-up-a-backup-location-for-lync-server-2013"></a><span data-ttu-id="9c4dc-103">Configuration d’un emplacement de sauvegarde pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c4dc-103">Setting up a backup location for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c4dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c4dc-104">

<span> </span></span></span>

<span data-ttu-id="9c4dc-105">_**Dernière modification de la rubrique :** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="9c4dc-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="9c4dc-106">Avant de procéder à la première sauvegarde de Lync Server, configurez le matériel et le logiciel dont vous avez besoin afin de stocker et de tenir à jour les sauvegardes.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-106">Before you take your first backup of Lync Server, set up the hardware and software that you need in order to store and maintain the backups.</span></span> <span data-ttu-id="9c4dc-107">Vous devez obtenir l’accès au contenu multimédia et au contenu, le cas échéant, et fournir une connectivité réseau entre chaque serveur à sauvegarder et le média de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-107">You need to obtain access to the media and content, as appropriate, and provide network connectivity between each server to be backed up and the backup media.</span></span> <span data-ttu-id="9c4dc-108">Le média et l’emplacement que vous utilisez doivent être définis dans votre stratégie de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-108">The media and location that you use should be defined in your backup and restoration strategy.</span></span> <span data-ttu-id="9c4dc-109">L’emplacement que vous utilisez pour les sauvegardes régulières peut être local ou distant, mais il doit être accessible pour la sauvegarde et la restauration.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-109">The location that you use for regular backups can be local or remote, but it must be secure, and it must be accessible for both backup and restoration.</span></span> <span data-ttu-id="9c4dc-110">Nous vous recommandons d’utiliser un lieu distant pour vous protéger contre un événement catastrophique sur votre site principal.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-110">We recommend using a remote location to protect against a catastrophic event at your primary site.</span></span>

<span data-ttu-id="9c4dc-111">Après avoir configuré et testé les composants individuels, vérifiez l’accessibilité des sauvegardes sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="9c4dc-111">After you set up and test the individual components, verify accessibility to the backups from each server.</span></span>

<span data-ttu-id="9c4dc-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c4dc-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

