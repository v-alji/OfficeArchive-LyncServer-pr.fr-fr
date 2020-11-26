---
title: Résumé de port-Fédération de protocoles de messagerie extensible et de présence
description: 'Résumé de port : Fédération de port et de présence.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442802"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="f6fc9-103">Service de synthèse de port-extension de messagerie (XMPP) dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6fc9-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6fc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6fc9-104">

<span> </span></span></span>

<span data-ttu-id="f6fc9-105">_**Dernière modification de la rubrique :** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="f6fc9-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="f6fc9-106">Les ports et protocoles définis pour le proxy d’extension de messagerie et de présence (XMPP) déployés sur le serveur Edge autorisent les communications du partenaire fédéré de XMPP au serveur Edge et permettent également la communication entre votre serveur Edge et le partenaire fédéré de XMPP.</span><span class="sxs-lookup"><span data-stu-id="f6fc9-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="f6fc9-107">Une règle est également définie pour le pare-feu à l’intérieur du serveur frontal ou du pool frontal du serveur Edge ou du pool Edge.</span><span class="sxs-lookup"><span data-stu-id="f6fc9-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="f6fc9-108">Résumé du pare-feu pour le protocole extensible de messagerie et de présence</span><span class="sxs-lookup"><span data-stu-id="f6fc9-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6fc9-109">Protocole/TCP ou UDP/Port</span><span class="sxs-lookup"><span data-stu-id="f6fc9-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="f6fc9-110">Source (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="f6fc9-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="f6fc9-111">Destination (adresse IP)</span><span class="sxs-lookup"><span data-stu-id="f6fc9-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="f6fc9-112">Commentaires</span><span class="sxs-lookup"><span data-stu-id="f6fc9-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6fc9-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f6fc9-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-114">Indifférente</span><span class="sxs-lookup"><span data-stu-id="f6fc9-114">Any</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-115">Adresse IP de l’interface du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="f6fc9-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-116">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="f6fc9-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="f6fc9-117">Autorise la communication au proxy de serveur Edge XMPP auprès des partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="f6fc9-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6fc9-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="f6fc9-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-119">Adresse IP de l’interface du service Edge d’accès</span><span class="sxs-lookup"><span data-stu-id="f6fc9-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-120">Indifférente</span><span class="sxs-lookup"><span data-stu-id="f6fc9-120">Any</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-121">Port de communication serveur à serveur standard pour XMPP.</span><span class="sxs-lookup"><span data-stu-id="f6fc9-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="f6fc9-122">Autorise la communication du proxy de serveur Edge XMPP aux partenaires XMPP fédérés</span><span class="sxs-lookup"><span data-stu-id="f6fc9-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6fc9-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="f6fc9-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-124">Indifférente</span><span class="sxs-lookup"><span data-stu-id="f6fc9-124">Any</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-125">Adresse IP de l’interface du serveur Edge interne</span><span class="sxs-lookup"><span data-stu-id="f6fc9-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="f6fc9-126">Trafic de XMPP interne provenant de la passerelle XMPP du serveur frontal ou du pool frontal sur le serveur Edge</span><span class="sxs-lookup"><span data-stu-id="f6fc9-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f6fc9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6fc9-127">See Also</span></span>


[<span data-ttu-id="f6fc9-128">Exemple de configuration XMPP dans Lync Server 2013 – Fédération XMPP avec Google Talk</span><span class="sxs-lookup"><span data-stu-id="f6fc9-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="f6fc9-129">Gestion des partenaires fédérés XMPP dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6fc9-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="f6fc9-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6fc9-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

