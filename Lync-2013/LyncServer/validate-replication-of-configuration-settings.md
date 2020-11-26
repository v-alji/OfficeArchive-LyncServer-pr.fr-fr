---
title: Valider la réplication des paramètres de configuration
description: Valider la réplication des paramètres de configuration
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Validate replication of configuration settings
ms:assetid: 81a3c21d-b28a-4287-adac-11791e8db56d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205042(v=OCS.15)
ms:contentKeyID: 48184663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26d8e9326da8b865f4e2ca3181975fb899300636
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446534"
---
# <a name="validate-replication-of-configuration-settings"></a><span data-ttu-id="3a604-103">Valider la réplication des paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="3a604-103">Validate replication of configuration settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3a604-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3a604-104">

<span> </span></span></span>

<span data-ttu-id="3a604-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3a604-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3a604-106">Vous pouvez valider la réplication des informations de configuration sur le serveur Edge en exécutant l’applet de contrôle Lync Server 2013 **Get-CsManagementStoreReplicationStatus** sur l’ordinateur interne sur lequel se trouve la Banque centrale de gestion ou n’importe quel ordinateur appartenant à un domaine sur lequel les composants principaux de Lync Server 2013 sont installés.</span><span class="sxs-lookup"><span data-stu-id="3a604-106">You can validate the replication of configuration information to the Edge Server by running the Lync Server 2013 **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located or any domain joined computer on which Lync Server 2013 Core Components is installed.</span></span>

<span data-ttu-id="3a604-107">Les résultats initiaux risquent d’indiquer l’état « false » au lieu de « true » pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="3a604-107">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="3a604-108">Si tel est le cas, exécutez l’applet de connexion **Invoke-CsManagementStoreReplication** et attendez la fin de la réplication avant d’exécuter de nouveau l’applet de connexion **Get-CsManagementStoreReplicationStatus** .</span><span class="sxs-lookup"><span data-stu-id="3a604-108">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** cmdlet again.</span></span>

<span data-ttu-id="3a604-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3a604-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

