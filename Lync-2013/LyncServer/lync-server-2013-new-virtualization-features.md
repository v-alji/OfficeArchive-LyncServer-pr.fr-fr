---
title: 'Lync Server 2013 : Nouvelles fonctionnalités de virtualisation'
description: 'Lync Server 2013 : nouvelles fonctionnalités de virtualisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New virtualization features
ms:assetid: edeb2c41-765e-47b8-8a2b-7a7ce09de2ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721926(v=OCS.15)
ms:contentKeyID: 49733861
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac15b8592d158d84807ff9e665dd6da50b699059
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424981"
---
# <a name="new-virtualization-features-in-lync-server-2013"></a><span data-ttu-id="d8be1-103">Nouvelles fonctionnalités de virtualisation dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8be1-103">New virtualization features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8be1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8be1-104">

<span> </span></span></span>

<span data-ttu-id="d8be1-105">_**Dernière modification de la rubrique :** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="d8be1-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="d8be1-106">Lync Server 2013 prend en charge la virtualisation sur Windows Server 2012, Windows Server 2012 R2 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d8be1-106">Lync Server 2013 supports virtualization on both Windows Server 2012, Windows Server 2012 R2, and Windows Server 2008 R2.</span></span> <span data-ttu-id="d8be1-107">La prise en charge de Windows Server 2012 et de Windows Server 2012 R2 inclut la prise en charge des fonctionnalités de virtualisation d’e/s racines uniques (SR-IOV).</span><span class="sxs-lookup"><span data-stu-id="d8be1-107">Support on Windows Server 2012 and Windows Server 2012 R2 includes support for the Single Root I/O Virtualization (SR-IOV) capabilities.</span></span> <span data-ttu-id="d8be1-108">Avec SR-IOV, la fonction virtuelle d’une carte de réseau physique est affectée directement à une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d8be1-108">With SR-IOV, the virtual function of a physical network adapter is assigned directly to a virtual machine.</span></span> <span data-ttu-id="d8be1-109">Cela augmente le débit du réseau et permet de réduire la latence du réseau tout en réduisant la surcharge de l’UC hôte requise pour le traitement du trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="d8be1-109">This increases network throughput and reduces network latency while also reducing the host CPU overhead that is required for processing network traffic.</span></span> <span data-ttu-id="d8be1-110">Pour tirer parti de SR-IOV, vous devez utiliser un serveur hôte qui prend en charge SR-IOV, ainsi que les cartes réseau qui prennent en charge le SR-IOV.</span><span class="sxs-lookup"><span data-stu-id="d8be1-110">To take advantage of SR-IOV, you must use a host server which has BIOS which supports SR-IOV, as well as use network adapters that support SR-IOV.</span></span>

<span data-ttu-id="d8be1-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8be1-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

