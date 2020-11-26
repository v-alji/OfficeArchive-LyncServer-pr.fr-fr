---
title: 'Lync Server 2013 : Nouvelle fonctionnalité de jonction'
description: 'Lync Server 2013 : nouvelle fonctionnalité de Trunk.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New trunk feature
ms:assetid: 9b398bc8-2760-4218-b1a4-89b9694b1171
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688152(v=OCS.15)
ms:contentKeyID: 49733755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8f923ceada899608cc350bd1343345c12d0996b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445336"
---
# <a name="new-trunk-feature-in-lync-server-2013"></a><span data-ttu-id="bd042-103">Nouvelle fonctionnalité de jonction dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd042-103">New trunk feature in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd042-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd042-104">

<span> </span></span></span>

<span data-ttu-id="bd042-105">_**Dernière modification de la rubrique :** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="bd042-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="bd042-106">Dans Microsoft Lync Server 2013, plusieurs ISL entre un serveur de médiation et une passerelle peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="bd042-106">In Microsoft Lync Server 2013, multiple trunks between a Mediation Server and a gateway can be defined.</span></span> <span data-ttu-id="bd042-107">Microsoft Lync Server 2010 uniquement autorisé pour une ISL unique entre un serveur de médiation et une passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="bd042-107">Microsoft Lync Server 2010 only allowed for a single trunk between a Mediation Server and a PSTN gateway.</span></span> <span data-ttu-id="bd042-108">Cette fonctionnalité permet de définir davantage de Trunks.</span><span class="sxs-lookup"><span data-stu-id="bd042-108">This feature provides the flexibility to define additional trunks.</span></span> <span data-ttu-id="bd042-109">Un Trunk est une association logique entre un nom de domaine complet du serveur de médiation et un port d’écoute et un nom de domaine complet et un port d’écoute de la passerelle PSTN.</span><span class="sxs-lookup"><span data-stu-id="bd042-109">A trunk is a logical association between a Mediation Server FQDN and listening port and a PSTN gateway FQDN and listening port.</span></span> <span data-ttu-id="bd042-110">Cette nouvelle fonctionnalité permet de définir facilement le Trunk de résilience (qui permet d’utiliser plusieurs serveurs de médiation pour acheminer les appels vers la même passerelle RTC). pour l’interopérabilité avec le protocole PBX, dans lequel plusieurs lignes associées à différentes stratégies associées peuvent être utilisées entre le PBX IP et un serveur de médiation, et pour les configurations SIP Trunk où les serveurs de médiation sur les différents sites disposent de lignes SIP sur l’opérateur référencées par le même nom de domaine complet du transporteur.</span><span class="sxs-lookup"><span data-stu-id="bd042-110">This new capability allows for easy trunk definition for resiliency (where multiple Mediation Servers can be used to route calls to the same PSTN Gateway), for PBX interoperability, where multiple trunks with different associated policies can be used between and IP-PBX and a Mediation Server, and for SIP trunk configurations where Mediation Servers at different sites have SIP trunks to the carrier referenced by the same carrier FQDN.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="bd042-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd042-111">See Also</span></span>


[<span data-ttu-id="bd042-112">Nouvelles fonctionnalités Voix Entreprise dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd042-112">New Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-new-enterprise-voice-features.md)  
  

<span data-ttu-id="bd042-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd042-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

