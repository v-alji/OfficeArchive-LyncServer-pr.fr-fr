---
title: 'Lync Server 2013 : Enhanced 9-1-1 (E9-1-1) et serveur de médiation'
description: 'Lync Server 2013 : Enhanced 9-1-1 (E9-1-1) et Mediation Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enhanced 9-1-1 (E9-1-1) and Mediation Server
ms:assetid: d231221f-5596-4a87-a463-269f5bcce65f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398903(v=OCS.15)
ms:contentKeyID: 48185448
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fb6da8e69883e321f23a53e8dc5067817d5aa66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428628"
---
# <a name="enhanced-9-1-1-e9-1-1-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="98937-103">Enhanced 9-1-1 (E9-1-1) et serveur de médiation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98937-103">Enhanced 9-1-1 (E9-1-1) and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98937-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98937-104">

<span> </span></span></span>

<span data-ttu-id="98937-105">_**Dernière modification de la rubrique :** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="98937-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="98937-106">Le serveur de médiation dispose de fonctionnalités étendues afin qu’il puisse interagir correctement avec les fournisseurs de services 9-1-1 (E9-1-1) améliorés.</span><span class="sxs-lookup"><span data-stu-id="98937-106">The Mediation Server has extended capabilities so that it can correctly interact with Enhanced 9-1-1 (E9-1-1) service providers.</span></span> <span data-ttu-id="98937-107">Aucune configuration spéciale n’est nécessaire sur le serveur de médiation ; les extensions SIP requises pour l’interaction E9-1-1 sont par défaut incluses dans le protocole SIP du serveur de médiation pour ses interactions avec un homologue de passerelle (passerelle RTC, PBX IP ou l’SBC d’un fournisseur de services de téléphonie Internet, y compris les fournisseurs de services E9-1-1)</span><span class="sxs-lookup"><span data-stu-id="98937-107">No special configuration is needed on the Mediation Server; the SIP extensions required for E9-1-1 interaction are, by default, included in the Mediation Server’s SIP protocol for its interactions with a gateway peer (PSTN gateway, IP-PBX, or the SBC of an Internet Telephony Service Provider, including E9-1-1 Service Providers)</span></span>

<span data-ttu-id="98937-108">Le trunking SIP pour un fournisseur de services E9-1-1 peut être arrêté sur un pool de serveurs de médiation existant ou exiger des serveurs de médiation autonomes, selon que l’élément SBC E9-1-1 peut interagir avec un pool de serveurs de médiation.</span><span class="sxs-lookup"><span data-stu-id="98937-108">Whether the SIP trunk to an E9-1-1 Service Provider can be terminated on an existing Mediation Server pool or will require stand-alone Mediation Servers will depend on whether the E9-1-1 SBC can interact with a pool of Mediation Servers.</span></span> <span data-ttu-id="98937-109">Pour plus d’informations, consultez [M :N Trunk dans Lync Server 2013](lync-server-2013-m-n-trunk.md).</span><span class="sxs-lookup"><span data-stu-id="98937-109">For details, see [M:N trunk in Lync Server 2013](lync-server-2013-m-n-trunk.md).</span></span>

<span data-ttu-id="98937-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98937-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

