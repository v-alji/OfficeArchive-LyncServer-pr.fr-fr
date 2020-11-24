---
title: 'Lync Server 2013 : Association de sous-réseaux avec les sites réseau pour le CAC'
description: 'Lync Server 2013 : associez des sous-réseaux aux sites réseau pour le CAC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for CAC
ms:assetid: a749c9b3-15f3-4e74-9f43-1507d3c2c940
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412786(v=OCS.15)
ms:contentKeyID: 48185017
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d68607c1674bb964c27c8408583be7f5e092f4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395169"
---
# <a name="associate-subnets-with-network-sites-for-cac-in-lync-server-2013"></a><span data-ttu-id="29704-103">Associez des sous-réseaux aux sites réseau pour le CAC dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="29704-103">Associate subnets with network sites for CAC in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="29704-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="29704-104">

<span> </span></span></span>

<span data-ttu-id="29704-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="29704-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="29704-106">Chaque sous-réseau de votre réseau doit être associé à un site réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="29704-106">Every subnet in your network must be associated with a specific network site.</span></span> <span data-ttu-id="29704-107">En effet, les informations de sous-réseau permettent de déterminer le site réseau sur lequel se trouve un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="29704-107">This is because subnet information is used to determine the network site on which an endpoint is located.</span></span> <span data-ttu-id="29704-108">Lorsque les deux parties d’une session sont connues, le contrôle d’admission des appels (CAC) peut déterminer s’il y a suffisamment de bande passante pour établir un appel.</span><span class="sxs-lookup"><span data-stu-id="29704-108">When the locations of both parties in a session are known, call admission control (CAC) can determine if there is sufficient bandwidth to establish a call.</span></span>

<span data-ttu-id="29704-109">Le contrôle d’admission des appels n’a aucune configuration spéciale pour l’Association de sous-réseaux aux sites réseau.</span><span class="sxs-lookup"><span data-stu-id="29704-109">Call admission control does not have any special requirements for associating subnets with network sites.</span></span> <span data-ttu-id="29704-110">Pour créer une association entre les sous-réseaux et les sites réseau dans votre topologie, suivez les procédures décrites dans [associer un sous-réseau à un site réseau dans Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="29704-110">To create an association between the subnets and network sites in your topology, follow the procedures in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span> <span data-ttu-id="29704-111">Pour afficher les sites réseau (et leurs sous-réseaux correspondants) dans l’exemple de topologie réseau pour le contrôle d’admission des appels, voir [exemple : rassemblement de vos exigences de contrôle d’admission des appels dans Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="29704-111">To view the network sites (and their respective subnets) in the example network topology for call admission control, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="29704-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="29704-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

