---
title: Prise en charge du matériel de périphérique dans Lync Server 2013
description: Prise en charge du matériel du périphérique Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429449"
---
# <a name="device-hardware-support-in-lync-server-2013"></a><span data-ttu-id="cda31-103">Prise en charge du matériel de périphérique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cda31-103">Device hardware support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cda31-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cda31-104">

<span> </span></span></span>

<span data-ttu-id="cda31-105">_**Dernière modification de la rubrique :** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="cda31-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="cda31-106">Des configurations matérielles spécifiques doivent être en place avant le déploiement de téléphones IP et d’appareils analogiques.</span><span class="sxs-lookup"><span data-stu-id="cda31-106">Specific hardware configurations must be in place before you deploy IP phones and analog devices.</span></span>

<span data-ttu-id="cda31-107">Les téléphones IP exécutant Lync Phone Edition prennent en charge la découverte des couches de liaison Protocol-Media point de terminaison (LLDP-MED) et Power over Ethernet (PoE).</span><span class="sxs-lookup"><span data-stu-id="cda31-107">IP phones running Lync Phone Edition support Link Layer Discovery Protocol-Media Endpoint Discovery (LLDP-MED) and Power over Ethernet (PoE).</span></span> <span data-ttu-id="cda31-108">Pour tirer parti de LLDP-MED, le commutateur doit prendre en charge les normes IEEE 802.1 AB et ANSI/TIA-1057.</span><span class="sxs-lookup"><span data-stu-id="cda31-108">To take advantage of LLDP-MED, the switch must support IEEE802.1AB and ANSI/TIA-1057.</span></span> <span data-ttu-id="cda31-109">Pour tirer parti de la PoE, le commutateur doit prendre en charge le mode PoE 802.3 AF ou 802.3 au.</span><span class="sxs-lookup"><span data-stu-id="cda31-109">To take advantage of PoE, the switch must support PoE802.3AF or 802.3at.</span></span>

<span data-ttu-id="cda31-110">Pour activer LLDP-MED, l’administrateur doit activer LLDP en utilisant la fenêtre console de basculement et définir la stratégie réseau LLDP-MED avec l’ID VLAN valide.</span><span class="sxs-lookup"><span data-stu-id="cda31-110">To enable LLDP-MED, the administrator must enable LLDP by using the switch console window and set the LLDP-MED network policy with the correct voice VLAN ID.</span></span>

<span data-ttu-id="cda31-111">De plus, si votre déploiement inclut des appareils analogiques, vous devez configurer la passerelle analogique pour utiliser Lync Server et la passerelle doit être l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="cda31-111">In addition, if your deployment includes analog devices, you must configure the analog gateway to use Lync Server, and the gateway must be one of the following:</span></span>

  - <span data-ttu-id="cda31-112">Un adaptateur de téléphone analogique (ATA)</span><span class="sxs-lookup"><span data-stu-id="cda31-112">An analog telephone adapter (ATA)</span></span>

  - <span data-ttu-id="cda31-113">Passerelle analogique PSTN</span><span class="sxs-lookup"><span data-stu-id="cda31-113">A PSTN analog gateway</span></span>

  - <span data-ttu-id="cda31-114">Une unité de branchement Survivable qui inclut une passerelle analogique PSTN</span><span class="sxs-lookup"><span data-stu-id="cda31-114">A Survivable Branch Appliance that includes a PSTN analog gateway</span></span>

  - <span data-ttu-id="cda31-115">Une unité de branchement Survivable qui inclut une passerelle RTC qui communique avec un disque ATA</span><span class="sxs-lookup"><span data-stu-id="cda31-115">A Survivable Branch Appliance that includes a PSTN gateway that communicates with an ATA</span></span>

<span data-ttu-id="cda31-116">Pour plus d’informations sur la configuration d’une passerelle analogique, voir la section « planification de déploiement de périphériques analogiques » [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) dans la bibliothèque TechNet de Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="cda31-116">To learn how to configure an analog gateway, see "Planning to Deploy Analog Devices" at [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="cda31-117">(Les appareils analogiques fonctionnent de la même manière dans Lync Server 2013 que dans Lync Server 2010.)</span><span class="sxs-lookup"><span data-stu-id="cda31-117">(Analog devices work the same way in Lync Server 2013 as they do in Lync Server 2010.)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cda31-118">Si le commutateur prend en charge cette option, vous pouvez configurer le commutateur pour Enhanced 9-1-1 (E9-1-1).</span><span class="sxs-lookup"><span data-stu-id="cda31-118">You can configure the switch for Enhanced 9-1-1 (E9-1-1), if the switch supports this.</span></span>



<span data-ttu-id="cda31-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cda31-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

