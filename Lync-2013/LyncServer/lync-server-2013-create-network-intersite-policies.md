---
title: 'Lync Server 2013 : création de stratégies d’intersite réseau'
description: 'Lync Server 2013 : création de stratégies d’intersite réseau.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9666efcb9c6da459a8e50eeae66cd1a513b46f65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431938"
---
# <a name="create-network-intersite-policies-in-lync-server-2013"></a><span data-ttu-id="f175e-103">Créer des stratégies d’intersite réseau dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f175e-103">Create network intersite policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f175e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f175e-104">

<span> </span></span></span>

<span data-ttu-id="f175e-105">_**Dernière modification de la rubrique :** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="f175e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="f175e-106">Une *stratégie d’intersite réseau* définit des limitations de bande passante entre les sites disposant de liens WAN directs entre eux.</span><span class="sxs-lookup"><span data-stu-id="f175e-106">A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.</span></span>

<span data-ttu-id="f175e-107">Pour plus d’informations, reportez-vous à la documentation Lync Server Management Shell pour les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="f175e-107">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="f175e-108">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="f175e-108">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="f175e-109">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="f175e-109">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="f175e-110">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="f175e-110">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)

  - [<span data-ttu-id="f175e-111">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="f175e-111">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f175e-112">Une stratégie d’intersite réseau est requise <EM>uniquement</EM> s’il existe un lien croisé direct entre deux sites du réseau.</span><span class="sxs-lookup"><span data-stu-id="f175e-112">A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.</span></span>



</div>

<span data-ttu-id="f175e-113">Dans la région Amérique du Nord de l’exemple de topologie, il existe un lien direct entre les sites Reno et Albuquerque.</span><span class="sxs-lookup"><span data-stu-id="f175e-113">In the example topology North America region, there is a direct link between the Reno and Albuquerque sites.</span></span> <span data-ttu-id="f175e-114">Ces deux sites nécessitent une stratégie de intersite qui applique un profil de stratégie de bande passante approprié.</span><span class="sxs-lookup"><span data-stu-id="f175e-114">These two sites require an intersite policy that applies an appropriate bandwidth policy profile.</span></span> <span data-ttu-id="f175e-115">L’exemple suivant applique le \_ profil de liaison 20Mo.</span><span class="sxs-lookup"><span data-stu-id="f175e-115">The following example applies the 20Mb\_Link profile.</span></span>

<div>

## <a name="to-create-a-network-intersite-policy"></a><span data-ttu-id="f175e-116">Pour créer une stratégie d’intersite réseau</span><span class="sxs-lookup"><span data-stu-id="f175e-116">To create a network intersite policy</span></span>

1.  <span data-ttu-id="f175e-117">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="f175e-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="f175e-118">Exécutez l’applet de connexion New-CsNetworkInterSitePolicy pour créer des stratégies d’intersite réseau et appliquer un profil de stratégie de bande passante approprié pour deux sites qui disposent d’un lien direct.</span><span class="sxs-lookup"><span data-stu-id="f175e-118">Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link.</span></span> <span data-ttu-id="f175e-119">Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="f175e-119">For example, run:</span></span>
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  <span data-ttu-id="f175e-120">Répétez l’étape 2 autant de fois que nécessaire pour créer des stratégies d’intersite réseau pour toutes les paires de sites réseau qui présentent un lien croisé direct.</span><span class="sxs-lookup"><span data-stu-id="f175e-120">Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.</span></span>

<span data-ttu-id="f175e-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f175e-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

