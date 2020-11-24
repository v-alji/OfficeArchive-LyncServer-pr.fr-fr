---
title: 'Lync Server 2013 : Configuration des services Internet (IIS)'
description: 'Lync Server 2013 : configurer IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure IIS
ms:assetid: bc4ae8cc-ec0c-42f1-9034-058930e530d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412918(v=OCS.15)
ms:contentKeyID: 48185248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdd08e47d05f2e32f14178eaaa3a100f8c445dda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394772"
---
# <a name="configure-iis-for-lync-server-2013"></a><span data-ttu-id="78b27-103">Configuration des services Internet (IIS) pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78b27-103">Configure IIS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78b27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78b27-104">

<span> </span></span></span>

<span data-ttu-id="78b27-105">_**Dernière modification de la rubrique :** 2011-12-16_</span><span class="sxs-lookup"><span data-stu-id="78b27-105">_**Topic Last Modified:** 2011-12-16_</span></span>

<span data-ttu-id="78b27-106">La configuration d’Internet Information Services (IIS) pour Lync Server 2013 implique l’installation des composants appropriés pour prendre en charge les services Web requis par Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="78b27-106">Configuring Internet Information Services (IIS) for Lync Server 2013 involves installing the correct components to support the Web Services needed by Lync Server 2013.</span></span> <span data-ttu-id="78b27-107">Pour plus d’informations sur l’installation d’IIS, voir [configuration d’IIS dans Lync Server 2013](lync-server-2013-iis-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="78b27-107">For details about installing IIS, see [IIS configuration in Lync Server 2013](lync-server-2013-iis-configuration.md).</span></span> <span data-ttu-id="78b27-108">Si vous disposez d’une stratégie pour exécuter l’Assistant Configuration de la sécurité sur des serveurs avant de les mettre en service ou dans le cadre de votre maintenance, reportez-vous à la rubrique [réactiver le serveur après la configuration de la sécurité fermez les ports dans IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) pour plus d’informations sur les effets secondaires de l’exécution de l’Assistant pour fermer les ports sur une configuration IIS Lync 2013 Server</span><span class="sxs-lookup"><span data-stu-id="78b27-108">If you have a policy to run the Security Configuration Wizard on servers before putting them into service or as a typical part of your maintenance, see [Re-activate server after Security Configuration Wizard closes ports in IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) for information about a side effect of running the wizard that will close ports on a Lync Server 2013 IIS configuration.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="78b27-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="78b27-109">In This Section</span></span>

  - [<span data-ttu-id="78b27-110">Configuration des services Internet (IIS) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78b27-110">IIS configuration in Lync Server 2013</span></span>](lync-server-2013-iis-configuration.md)

  - [<span data-ttu-id="78b27-111">Réactivation du serveur après la fermeture des ports par l’Assistant Configuration de la sécurité dans les services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="78b27-111">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md)

<span data-ttu-id="78b27-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78b27-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

