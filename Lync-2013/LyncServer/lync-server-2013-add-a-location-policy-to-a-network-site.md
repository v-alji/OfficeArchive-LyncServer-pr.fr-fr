---
title: 'Lync Server 2013 : ajouter une stratégie d’emplacement à un site réseau'
description: 'Lync Server 2013 : ajoutez une stratégie d’emplacement à un site réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add a location policy to a network site
ms:assetid: 43bfab8a-3d6b-4ca4-8425-879fd910502e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425936(v=OCS.15)
ms:contentKeyID: 48183980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20f71d3144e2ef730de5dae46be16138b5d36c42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439395"
---
# <a name="add-a-location-policy-to-a-network-site-in-lync-server-2013"></a><span data-ttu-id="c7137-103">Ajouter une stratégie d’emplacement à un site réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c7137-103">Add a location policy to a network site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7137-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7137-104">

<span> </span></span></span>

<span data-ttu-id="c7137-105">_**Dernière modification de la rubrique :** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="c7137-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="c7137-106">Les exemples suivants montrent comment ajouter la stratégie d’emplacement **Redmond** définie dans [créer des stratégies d’emplacement dans Lync Server 2013](lync-server-2013-create-location-policies.md) à un site réseau existant et comment créer un nouveau site réseau qui utilise la stratégie de localisation **Redmond** .</span><span class="sxs-lookup"><span data-stu-id="c7137-106">The following examples show how to add the **Redmond** location policy defined in [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) to an existing network site and how to create a new network site that uses the **Redmond** location policy.</span></span>

<span data-ttu-id="c7137-107">Pour plus d’informations sur l’utilisation des sites réseau, voir la documentation Lync Server Management Shell pour les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7137-107">For details about working with network sites, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="c7137-108">**New-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="c7137-108">**New-CsNetworkSite**</span></span>

  - <span data-ttu-id="c7137-109">**Get-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="c7137-109">**Get-CsNetworkSite**</span></span>

  - <span data-ttu-id="c7137-110">**Set-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="c7137-110">**Set-CsNetworkSite**</span></span>

  - <span data-ttu-id="c7137-111">**Remove-CsNetworkSite**</span><span class="sxs-lookup"><span data-stu-id="c7137-111">**Remove-CsNetworkSite**</span></span>

<div>

## <a name="to-assign-a-location-policy-to-an-existing-network-site"></a><span data-ttu-id="c7137-112">Pour affecter une stratégie d’emplacement à un site réseau existant</span><span class="sxs-lookup"><span data-stu-id="c7137-112">To assign a location policy to an existing network site</span></span>

1.  <span data-ttu-id="c7137-113">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="c7137-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="c7137-114">Exécutez les applets de commande suivantes pour modifier un site réseau existant.</span><span class="sxs-lookup"><span data-stu-id="c7137-114">Run the following cmdlets to modify an existing network site.</span></span>
    
    <span data-ttu-id="c7137-115">Affectez la stratégie d’emplacement balisée **Redmond** à un site réseau existant appelé **Redmond**.</span><span class="sxs-lookup"><span data-stu-id="c7137-115">Assign the **Redmond** tagged Location policy to an existing network site named **Redmond**.</span></span>
    
        Set-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

</div>

<div>

## <a name="to-assign-a-location-policy-to-a-new-network-site"></a><span data-ttu-id="c7137-116">Pour affecter une stratégie d’emplacement à un nouveau site réseau</span><span class="sxs-lookup"><span data-stu-id="c7137-116">To assign a location policy to a new network site</span></span>

1.  <span data-ttu-id="c7137-117">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="c7137-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="c7137-118">Exécutez l’applet de commande suivante pour créer un nouveau site réseau.</span><span class="sxs-lookup"><span data-stu-id="c7137-118">Run the following cmdlet to create a new network site.</span></span>
    
    <span data-ttu-id="c7137-119">Créez un site réseau dans la région réseau et affectez la stratégie d’emplacement balisée **Redmond**.</span><span class="sxs-lookup"><span data-stu-id="c7137-119">Create a new network site in the network region and assign the **Redmond** tagged Location policy.</span></span>
    
        New-CsNetworkSite -Identity "Redmond" -NetworkRegionID "NorthAmerica" -LocationPolicy "Redmond"

<span data-ttu-id="c7137-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7137-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

