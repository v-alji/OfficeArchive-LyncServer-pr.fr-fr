---
title: 'Lync Server 2013 : Détermination de la configuration système requise'
description: 'Lync Server 2013 : Déterminez la configuration système requise.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determining your system requirements
ms:assetid: 620e81e2-42df-4eda-8498-bd56a14aa0e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398438(v=OCS.15)
ms:contentKeyID: 48184286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ceca8eabb234ae7fd483372ff5e611664ecc4fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429488"
---
# <a name="determining-your-system-requirements-for-lync-server-2013"></a><span data-ttu-id="642a4-103">Détermination de la configuration système requise pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-103">Determining your system requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="642a4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="642a4-104">

<span> </span></span></span>

<span data-ttu-id="642a4-105">_**Dernière modification de la rubrique :** 2014-01-02_</span><span class="sxs-lookup"><span data-stu-id="642a4-105">_**Topic Last Modified:** 2014-01-02_</span></span>

<span data-ttu-id="642a4-106">Tous les serveurs exécutant Lync Server doivent disposer de la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="642a4-106">All servers running Lync Server must meet certain minimum system requirements.</span></span> <span data-ttu-id="642a4-107">La configuration requise pour Lync Server inclut le matériel du serveur, le système d’exploitation à installer sur chaque serveur, ainsi que les configurations logicielles associées, telles que les mises à jour Windows et les autres logiciels qui doivent être installés sur les serveurs.</span><span class="sxs-lookup"><span data-stu-id="642a4-107">System requirements for Lync Server include the server hardware, the operating system to be installed on each server, and related software requirements, such as the Windows updates and other software that must be installed on the servers.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="642a4-108">Lync Server est disponible uniquement dans une version 64 bits, qui nécessite le matériel 64 bits et une édition 64 bits de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="642a4-108">Lync Server is available only in a 64-bit edition, which requires 64-bit hardware and a 64-bit edition of Windows Server.</span></span> <span data-ttu-id="642a4-109">Il s’agit de l’outil de planification Microsoft Lync Server 2013, qui est disponible dans une édition 32 bits.</span><span class="sxs-lookup"><span data-stu-id="642a4-109">The exception is the Microsoft Lync Server 2013, Planning Tool, which is available in a 32-bit edition.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="642a4-110">Pour plus d’informations sur la prise en charge d’Active Directory, des topologies prises en charge, la colocalisation des serveurs et d’autres problèmes de prise en charge, voir <A href="lync-server-2013-supportability.md">prise en charge de Lync server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="642a4-110">For details about Active Directory support, supported topologies, server collocation, and other supportability issues, see <A href="lync-server-2013-supportability.md">Supportability for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="642a4-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="642a4-111">In This Section</span></span>

  - [<span data-ttu-id="642a4-112">Server Hardware Platforms pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-112">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)

  - [<span data-ttu-id="642a4-113">Prise en charge du système d’exploitation pour le serveur et les outils dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-113">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)

  - [<span data-ttu-id="642a4-114">Prise en charge du logiciel de base de données dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-114">Database software support in Lync Server 2013</span></span>](lync-server-2013-database-software-support.md)

  - [<span data-ttu-id="642a4-115">Autre configuration logicielle requise pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-115">Additional software requirements for Lync Server 2013</span></span>](lync-server-2013-additional-software-requirements.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="642a4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="642a4-116">See Also</span></span>


[<span data-ttu-id="642a4-117">Prise en charge du matériel client et du périphérique dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-117">Client and device hardware support in Lync Server 2013</span></span>](lync-server-2013-client-and-device-hardware-support.md)  
[<span data-ttu-id="642a4-118">Prise en charge pour Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="642a4-118">Supportability for Lync Server 2013</span></span>](lync-server-2013-supportability.md)  
  

<span data-ttu-id="642a4-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="642a4-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

