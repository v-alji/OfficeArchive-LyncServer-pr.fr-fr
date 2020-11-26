---
title: 'Lync Server 2013 : Restauration du contenu d’une conférence avec le service de sauvegarde'
description: 'Lync Server 2013 : restauration du contenu de la Conférence à l’aide du service de sauvegarde.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442543"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="0b2cf-103">Restauration du contenu d’une conférence avec le service de sauvegarde dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b2cf-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b2cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b2cf-104">

<span> </span></span></span>

<span data-ttu-id="0b2cf-105">_**Dernière modification de la rubrique :** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0b2cf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0b2cf-106">Si les informations de la Conférence stockées dans le magasin de fichiers d’un pool frontal deviennent indisponibles.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="0b2cf-107">vous devez restaurer ces informations de sorte que les utilisateurs hébergés sur le pool conservent leurs données de conférence.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="0b2cf-108">Si le pool frontal qui a perdu les données de conférence est associé à un autre pool frontal, vous pouvez utiliser le service de sauvegarde pour restaurer les données.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="0b2cf-109">Vous devez également effectuer cette tâche si un pool entier a échoué et que vous devez faire basculer ses utilisateurs vers un pool de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="0b2cf-110">Lorsque les utilisateurs ont basculé vers leur pool d’origine, vous devez utiliser cette procédure pour copier le contenu de la Conférence sur leur pool d’origine.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="0b2cf-111">Supposez que Pool1 est associé à Pool2, et les données de conférence en Pool1 sont perdues.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="0b2cf-112">Vous pouvez utiliser l’applet de commande suivante pour appeler le service de sauvegarde et restaurer le contenu :</span><span class="sxs-lookup"><span data-stu-id="0b2cf-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="0b2cf-113">La restauration du contenu de la Conférence risque de prendre un certain temps en fonction de la taille de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="0b2cf-114">Pour vérifier l’état du processus, vous pouvez utiliser l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2cf-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="0b2cf-115">Le processus est réalisé lorsque cette cmdlet renvoie une valeur d’état stable pour le module de conférence de données.</span><span class="sxs-lookup"><span data-stu-id="0b2cf-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="0b2cf-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b2cf-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

