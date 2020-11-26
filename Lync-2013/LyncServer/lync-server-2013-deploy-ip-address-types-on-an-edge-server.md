---
title: 'Lync Server 2013 : Déploiement des types d’adresse IP sur un serveur Edge'
description: 'Lync Server 2013 : déploiement de types d’adresse IP sur un serveur Edge.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy IP address types on an Edge Server
ms:assetid: 6e2fe7e8-6e90-4d1a-8fc5-e3be92c46571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204984(v=OCS.15)
ms:contentKeyID: 48184435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7798ca2f7b38865a2b4ea373546dd4e7203f5b8e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430198"
---
# <a name="deploy-ip-address-types-on-an-edge-server-for-lync-server-2013"></a><span data-ttu-id="c871c-103">Déploiement des types d’adresse IP sur un serveur Edge pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c871c-103">Deploy IP address types on an Edge Server for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c871c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c871c-104">

<span> </span></span></span>

<span data-ttu-id="c871c-105">_**Dernière modification de la rubrique :** 2012-06-14_</span><span class="sxs-lookup"><span data-stu-id="c871c-105">_**Topic Last Modified:** 2012-06-14_</span></span>

<span data-ttu-id="c871c-106">À l’aide du générateur de topologie, suivez les étapes décrites dans la procédure ci-dessous pour déployer des types d’adresse IP sur un serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="c871c-106">Using Topology Builder, perform the steps in the following procedure to deploy IP address types on an Edge Server.</span></span>

<div>

## <a name="to-deploy-ip-address-types-on-an-edge-server"></a><span data-ttu-id="c871c-107">Pour déployer des types d’adresses IP sur un serveur Edge</span><span class="sxs-lookup"><span data-stu-id="c871c-107">To deploy IP address types on an Edge Server</span></span>

1.  <span data-ttu-id="c871c-108">Dans le générateur de topologie, sous **pools de bords**, cliquez avec le bouton droit sur le serveur d’un pool, puis sélectionnez **modifier les propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c871c-108">In Topology Builder, under **Edge pools**, right-click the server within a pool, and then select **Edit Properties**.</span></span> <span data-ttu-id="c871c-109">(Vous pouvez également sélectionner le serveur, puis cliquer sur **Modifier les propriétés** à partir du menu **Action**.)</span><span class="sxs-lookup"><span data-stu-id="c871c-109">(Alternatively, select the server, and then click **Edit Properties** from the **Action** menu.)</span></span>

2.  <span data-ttu-id="c871c-p102">Dans la fenêtre **Modifier les propriétés**, sélectionnez la configuration d’adresse IP à prendre en charge. Les figures suivantes illustrent une configuration double pile pour l’interface interne et l’interface externe.</span><span class="sxs-lookup"><span data-stu-id="c871c-p102">In the **Edit Properties** window, select the IP address configuration that you want to support. The following figures show a dual stack configuration for the internal interface and the external interface.</span></span>
    
    <span data-ttu-id="c871c-112">**Interface interne de serveur Edge à double pile**</span><span class="sxs-lookup"><span data-stu-id="c871c-112">**Dual stacked Edge Server internal interface**</span></span>
    
    <span data-ttu-id="c871c-113">![Page des propriétés générales de Lync Server](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Page des propriétés générales de Lync Server")</span><span class="sxs-lookup"><span data-stu-id="c871c-113">![Lync Server general properties page](images/JJ204984.5b0883ee-b9f2-4a21-91a9-3286d0beb63b(OCS.15).png "Lync Server general properties page")</span></span>
    
    <span data-ttu-id="c871c-114">**Interface externe de serveur Edge à double pile**</span><span class="sxs-lookup"><span data-stu-id="c871c-114">**Dual stacked Edge Server external interface**</span></span>
    
    <span data-ttu-id="c871c-115">![Page tronçon suivant/configuration externe du serveur Lync](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Page tronçon suivant/configuration externe du serveur Lync")</span><span class="sxs-lookup"><span data-stu-id="c871c-115">![Lync Server next hop/external configuration page](images/JJ204984.2aa00ce2-ba50-40aa-bbf1-78636016daf9(OCS.15).png "Lync Server next hop/external configuration page")</span></span>

3.  <span data-ttu-id="c871c-116">Pour chaque type d’adresse sélectionné, vous devez fournir des adresses internes et externes appropriées.</span><span class="sxs-lookup"><span data-stu-id="c871c-116">For each address type that you select, you must supply appropriate internal and external addresses.</span></span>

<span data-ttu-id="c871c-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c871c-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

