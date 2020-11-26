---
title: Migrer des périphériques analogiques
description: Migration de périphériques analogiques.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443831"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="320a2-103">Migrer des périphériques analogiques</span><span class="sxs-lookup"><span data-stu-id="320a2-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="320a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="320a2-104">

<span> </span></span></span>

<span data-ttu-id="320a2-105">_**Dernière modification de la rubrique :** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="320a2-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="320a2-106">Lync Server prend en charge les appareils analogiques.</span><span class="sxs-lookup"><span data-stu-id="320a2-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="320a2-107">Plus précisément, les appareils analogiques pris en charge sont les téléphones analogiques et les Fax analogiques.</span><span class="sxs-lookup"><span data-stu-id="320a2-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="320a2-108">Vous pouvez configurer les passerelles qualifiées pour prendre en charge l’utilisation d’appareils analogiques dans votre environnement Lync Server.</span><span class="sxs-lookup"><span data-stu-id="320a2-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="320a2-109">Après avoir effectué une migration de Lync Server 2010 vers Lync Server 2013, vous devez également déplacer les objets de contact associés aux périphériques analogiques.</span><span class="sxs-lookup"><span data-stu-id="320a2-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="320a2-110">Utilisez Lync Server Management Shell pour récupérer tous les objets de contact associés aux appareils analogiques Lync Server 2010, puis déplacez ces objets vers le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="320a2-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="320a2-111">Pour migrer des périphériques analogiques</span><span class="sxs-lookup"><span data-stu-id="320a2-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="320a2-112">Démarrez Lync Server Management Shell : cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft Lync Server 2013**, puis sur **Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="320a2-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="320a2-113">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="320a2-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="320a2-114">Vérifiez que tous les objets de contact ont été déplacés vers le pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="320a2-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="320a2-115">À partir de la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="320a2-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="320a2-116">Vérifiez que tous les objets de contact sont désormais associés au pool Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="320a2-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="320a2-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="320a2-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

