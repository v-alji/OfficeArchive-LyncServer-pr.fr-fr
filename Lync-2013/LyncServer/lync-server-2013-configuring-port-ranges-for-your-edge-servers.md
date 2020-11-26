---
title: 'Lync Server 2013 : configuration de plages de ports pour vos serveurs Edge'
description: 'Lync Server 2013 : configuration de plages de ports pour vos serveurs de périphérie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Edge Servers
ms:assetid: 6f0ae442-6624-4e3f-849a-5b9e387fb8cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204996(v=OCS.15)
ms:contentKeyID: 48184469
ms.date: 07/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c085a5dbc32bbf56842984eae2ef8896ab895c65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432743"
---
# <a name="configuring-port-ranges-for-your-edge-servers-in-lync-server-2013"></a><span data-ttu-id="b8d03-103">Configuration de plages de ports pour vos serveurs Edge dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8d03-103">Configuring port ranges for your Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8d03-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8d03-104">

<span> </span></span></span>

<span data-ttu-id="b8d03-105">_**Dernière modification de la rubrique :** 2015-07-24_</span><span class="sxs-lookup"><span data-stu-id="b8d03-105">_**Topic Last Modified:** 2015-07-24_</span></span>

<span data-ttu-id="b8d03-106">Avec les serveurs Edge, vous n’avez pas besoin de configurer des plages de port distinctes pour le partage audio, vidéo et d’application. de même, les plages de port utilisées pour les serveurs Edge ne doivent pas nécessairement correspondre aux plages de port utilisées avec vos serveurs de conférence, d’application et de médiation.</span><span class="sxs-lookup"><span data-stu-id="b8d03-106">With Edge servers you do not have to configure separate port ranges for audio, video, and application sharing; likewise, the port ranges used for Edge servers do not have to match the port ranges used with your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="b8d03-107">Avant de continuer, nous vous conseillons d’insister sur le fait que, si vous dépassez cette option, nous vous conseillons de ne pas modifier les plages de ports, car cela peut nuire à certains scénarios si vous vous éloignez de la plage de ports 50000.</span><span class="sxs-lookup"><span data-stu-id="b8d03-107">Before we proceed with our example, it's important to stress that while this option exists, we do recommend you not change the port ranges, as this may adversely affect some scenarios if you move out of the 50000 port range.</span></span>

<span data-ttu-id="b8d03-108">Par exemple, supposons que vous ayez configuré vos serveurs de conférence, d’application et de médiation pour utiliser ces plages de ports :</span><span class="sxs-lookup"><span data-stu-id="b8d03-108">For example, suppose you have configured your Conferencing, Application, and Mediation servers to use these port ranges:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8d03-109">Type de paquet</span><span class="sxs-lookup"><span data-stu-id="b8d03-109">Packet Type</span></span></th>
<th><span data-ttu-id="b8d03-110">Port de démarrage</span><span class="sxs-lookup"><span data-stu-id="b8d03-110">Starting Port</span></span></th>
<th><span data-ttu-id="b8d03-111">Nombre de ports réservés</span><span class="sxs-lookup"><span data-stu-id="b8d03-111">Number of Ports Reserved</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8d03-112">Partage d'application</span><span class="sxs-lookup"><span data-stu-id="b8d03-112">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="b8d03-113">40803</span><span class="sxs-lookup"><span data-stu-id="b8d03-113">40803</span></span></p></td>
<td><p><span data-ttu-id="b8d03-114">8348</span><span class="sxs-lookup"><span data-stu-id="b8d03-114">8348</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8d03-115">Audio</span><span class="sxs-lookup"><span data-stu-id="b8d03-115">Audio</span></span></p></td>
<td><p><span data-ttu-id="b8d03-116">49152</span><span class="sxs-lookup"><span data-stu-id="b8d03-116">49152</span></span></p></td>
<td><p><span data-ttu-id="b8d03-117">8348</span><span class="sxs-lookup"><span data-stu-id="b8d03-117">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8d03-118">Vidéo</span><span class="sxs-lookup"><span data-stu-id="b8d03-118">Video</span></span></p></td>
<td><p><span data-ttu-id="b8d03-119">57500</span><span class="sxs-lookup"><span data-stu-id="b8d03-119">57500</span></span></p></td>
<td><p><span data-ttu-id="b8d03-120">8034</span><span class="sxs-lookup"><span data-stu-id="b8d03-120">8034</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8d03-121"><strong>Totaux</strong></span><span class="sxs-lookup"><span data-stu-id="b8d03-121"><strong>Totals</strong></span></span></p></td>
<td><p>--</p></td>
<td><p><span data-ttu-id="b8d03-122">24730</span><span class="sxs-lookup"><span data-stu-id="b8d03-122">24730</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8d03-123">Comme vous pouvez le constater, vos plages de port pour le partage audio, vidéo et d’application commencent au port 40803 et incluent au total des ports 24732.</span><span class="sxs-lookup"><span data-stu-id="b8d03-123">As you can see, your port ranges for audio, video, and application sharing start at port 40803 and encompass a total of 24732 ports.</span></span> <span data-ttu-id="b8d03-124">Si vous le souhaitez, vous pouvez configurer un serveur Edge donné pour utiliser ces valeurs de port globales en exécutant une commande similaire à celle-ci dans Lync Server Management Shell :</span><span class="sxs-lookup"><span data-stu-id="b8d03-124">If you prefer, you can configure a given Edge Server to use these overall port values by running a command similar to this one from within the Lync Server Management Shell:</span></span>

    Set-CsEdgeServer -Identity EdgeServer:atl-edge-001.litwareinc.com -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730

<span data-ttu-id="b8d03-125">Vous pouvez utiliser la commande suivante pour configurer simultanément tous les serveurs Edge de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="b8d03-125">Or, use the following command to simultaneously configure all the Edge Servers in your organization:</span></span>

    Get-CsService -EdgeServer | ForEach-Object {Set-CsEdgeServer -Identity $_.Identity -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730}

<span data-ttu-id="b8d03-126">Vous pouvez vérifier les paramètres de port actuels pour vos serveurs Edge à l’aide de la commande Lync Server Management Shell suivante :</span><span class="sxs-lookup"><span data-stu-id="b8d03-126">You can verify the current port settings for your Edge Servers by using this Lync Server Management Shell command:</span></span>

    Get-CsService -EdgeServer | Select-Object Identity, MediaCommunicationPortStart, MediaCommunicationPortCount

<span data-ttu-id="b8d03-127">Là encore, nous vous conseillons vivement de conserver les éléments tels que la configuration de port.</span><span class="sxs-lookup"><span data-stu-id="b8d03-127">Again, while we do provide these options, we strongly recommend you leave things as they are for the port configuration.</span></span>

<span data-ttu-id="b8d03-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8d03-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

