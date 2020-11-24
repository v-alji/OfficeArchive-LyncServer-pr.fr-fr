---
title: 'Lync Server 2013 : publier la base de données de localisation'
description: 'Lync Server 2013 : publier la base de données de localisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394564"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="6c6a4-103">Publier la base de données de localisation à partir de Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6c6a4-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6c6a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6c6a4-104">

<span> </span></span></span>

<span data-ttu-id="6c6a4-105">_**Dernière modification de la rubrique :** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="6c6a4-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="6c6a4-106">Le client ne pourra accéder aux nouveaux emplacements ajoutés à la base de données d’emplacements qu’une fois qu’ils seront publiés.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="6c6a4-107">Pour plus d’informations, consultez la documentation de Lync Server Management Shell pour l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6c6a4-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="6c6a4-108">**Publish-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="6c6a4-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="6c6a4-109">Si vous utilisez des passerelles ELIN, vous devez également charger les numéros d’identification de l’emplacement en cas d’urgence dans la base de données ALI (Automatic Location Identification) de votre opérateur de réseau téléphonique commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="6c6a4-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="6c6a4-110">Celui-ci peut exiger l’utilisation d’un format spécifique pour les enregistrements ELIN.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="6c6a4-111">Pour plus d’informations, contactez l’opérateur RTC.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="6c6a4-112">Vous pouvez exporter les enregistrements de la base de données de service d’information d’emplacement et les mettre en forme selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="6c6a4-113">Pour publier la base de données d’emplacements</span><span class="sxs-lookup"><span data-stu-id="6c6a4-113">To publish the location database</span></span>

  - <span data-ttu-id="6c6a4-114">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="6c6a4-115">Exécutez l’applet de commande ci-dessous pour publier la base de données d’emplacements.</span><span class="sxs-lookup"><span data-stu-id="6c6a4-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="6c6a4-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6c6a4-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

