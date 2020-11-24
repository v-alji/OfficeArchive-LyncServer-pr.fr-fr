---
title: 'Lync Server 2013 : Association de sous-réseaux avec les sites réseau pour la dérivation multimédia'
description: 'Lync Server 2013 : associez des sous-réseaux avec les sites réseau pour une dérivation multimédia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395164"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="8a16c-103">Associez des sous-réseaux aux sites réseau pour une dérivation multimédia dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a16c-103">Associate subnets with network sites for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a16c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a16c-104">

<span> </span></span></span>

<span data-ttu-id="8a16c-105">_**Dernière modification de la rubrique :** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="8a16c-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8a16c-106">Dans cette rubrique, nous partons du principe que vous avez configuré les paramètres globaux de contournement du média et que vous avez configuré la région du réseau et les sites réseau pour la dérivation multimédia.</span><span class="sxs-lookup"><span data-stu-id="8a16c-106">This topic assumes that you have configured media bypass global settings and that you have configured network region and network sites for media bypass.</span></span>



</div>

<span data-ttu-id="8a16c-107">Chaque sous-réseau de votre réseau doit être associé à un site réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="8a16c-107">Every subnet in your network must be associated with a specific network site.</span></span> <span data-ttu-id="8a16c-108">En effet, les informations de sous-réseau permettent de déterminer le site réseau sur lequel se trouve un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8a16c-108">This is because subnet information is used to determine the network site on which an endpoint is located.</span></span> <span data-ttu-id="8a16c-109">Lorsque les deux parties d’une session sont connues, l’exclusion de média peut déterminer l’endroit où envoyer du contenu multimédia pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="8a16c-109">When the locations of both parties in a session are known, media bypass can determine where to send media for processing.</span></span>

<span data-ttu-id="8a16c-110">La dérivation multimédia n’a aucune configuration particulière requise pour l’Association de sous-réseaux aux sites réseau.</span><span class="sxs-lookup"><span data-stu-id="8a16c-110">Media bypass does not have any special requirements for associating subnets with network sites.</span></span> <span data-ttu-id="8a16c-111">Pour créer une association entre les sous-réseaux et les sites réseau dans votre topologie, suivez les procédures décrites dans [associer un sous-réseau à un site réseau dans Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="8a16c-111">To create an association between the subnets and network sites in your topology, follow the procedures in [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a><span data-ttu-id="8a16c-112">Étapes suivantes : créer des profils de stratégie de bande passante</span><span class="sxs-lookup"><span data-stu-id="8a16c-112">Next Steps: Create Bandwidth Policy Profiles</span></span>

<span data-ttu-id="8a16c-113">Après avoir associé des sous-réseaux aux sites réseau pour le contournement du contenu multimédia, vous devez créer un ou plusieurs profils de stratégie de bande passante pour les partitionner en réseaux avec une bonne connectivité et ceux qui ne le sont pas, aux fins de contournement de média.</span><span class="sxs-lookup"><span data-stu-id="8a16c-113">After you associate subnets with network sites for media bypass, you must create one or more bandwidth policy profiles that will partition subnets into those with good connectivity and those without, for the purposes of media bypass.</span></span> <span data-ttu-id="8a16c-114">Tous les sous-réseaux au sein d’une région réseau qui n’ont pas de contraintes de bande passante disposent d’une bonne connectivité et, par conséquent, ces sous-réseaux peuvent utiliser une dérivation multimédia.</span><span class="sxs-lookup"><span data-stu-id="8a16c-114">All subnets within a network region with network sites that do not have bandwidth constraints have good connectivity, and, therefore, those subnets can use media bypass.</span></span>

<span data-ttu-id="8a16c-115">Pour plus d’instructions sur la configuration des profils de stratégie de bande passante, voir [créer des profils de stratégie de bande passante dans Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="8a16c-115">For procedures to configure bandwidth policy profiles, see [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).</span></span>

<span data-ttu-id="8a16c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a16c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

