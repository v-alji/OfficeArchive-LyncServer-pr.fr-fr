---
title: Vérifier les paramètres de configuration
description: Vérifiez les paramètres de configuration.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify configuration settings
ms:assetid: 51c2d1d9-63f7-43ab-88ca-b8913da7cede
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204885(v=OCS.15)
ms:contentKeyID: 48184111
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7bb1135e95dafe51e906768fe0f4f0d57bf2d6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423343"
---
# <a name="verify-configuration-settings"></a><span data-ttu-id="a1c70-103">Vérifier les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="a1c70-103">Verify configuration settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a1c70-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a1c70-104">

<span> </span></span></span>

<span data-ttu-id="a1c70-105">_**Dernière modification de la rubrique :** 2012-09-06_</span><span class="sxs-lookup"><span data-stu-id="a1c70-105">_**Topic Last Modified:** 2012-09-06_</span></span>

<span data-ttu-id="a1c70-106">Vous pouvez valider la réplication des informations de configuration sur le serveur Edge en exécutant l’applet de contrôle Lync Server 2013 **Get-CsManagementStoreReplicationStatus** sur l’ordinateur interne sur lequel se trouve la Banque centrale de gestion ou sur n’importe quel ordinateur sur lequel les composants principaux de lync Server 2013 (OcsCore.msi) sont installés.</span><span class="sxs-lookup"><span data-stu-id="a1c70-106">You can validate the replication of configuration information to the Edge server by running the Lync Server 2013 **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located, or on any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span>

<span data-ttu-id="a1c70-107">Les résultats initiaux risquent d’indiquer l’état « false » au lieu de « true » pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="a1c70-107">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="a1c70-108">Si tel est le cas, exécutez l’applet de connexion **Invoke-CsManagementStoreReplication** et attendez la fin de la réplication avant d’exécuter de nouveau **Get-CsManagementStoreReplicationStatus** .</span><span class="sxs-lookup"><span data-stu-id="a1c70-108">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="a1c70-109"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a1c70-109"></div>

<span> </span>

</div>

</div>

</span></span></div>

