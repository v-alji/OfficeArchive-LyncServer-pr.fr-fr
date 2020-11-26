---
title: 'Lync Server 2013 : Configuration de SQL Server'
description: 'Lync Server 2013 : configurer SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure SQL Server
ms:assetid: 84504918-cb4f-4b2f-be17-a70770b69025
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398669(v=OCS.15)
ms:contentKeyID: 48184699
ms.date: 01/22/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2330dc4548e5157b7f29567551df4c89ee15998b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433716"
---
# <a name="configure-sql-server-in-lync-server-2013"></a><span data-ttu-id="14019-103">Configuration de SQL Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14019-103">Configure SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14019-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14019-104">

<span> </span></span></span>

<span data-ttu-id="14019-105">_**Dernière modification de la rubrique :** 2015-01-22_</span><span class="sxs-lookup"><span data-stu-id="14019-105">_**Topic Last Modified:** 2015-01-22_</span></span>

<span data-ttu-id="14019-106">Pour chaque base de données que vous déployez, vous pouvez utiliser une instance SQL Server unique pour toutes les bases de données pour votre déploiement Lync Server 2013 qui peut être colocalisé sur un serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="14019-106">For each database that you deploy, you can use a single SQL Server instance for all databases for your Lync Server 2013 deployment that can be collocated on a database server.</span></span> <span data-ttu-id="14019-107">Pour plus d’informations sur la colocalisation de la base de données, consultez [prise en charge de la colocalisation des serveurs dans Lync server 2013](lync-server-2013-supported-server-collocation.md)</span><span class="sxs-lookup"><span data-stu-id="14019-107">For details about database collocation, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md) in the Supportability documentation.</span></span>

<span data-ttu-id="14019-108">Par ailleurs, chaque instance SQL Server doit être installée et disponible avant d’exécuter les étapes du générateur de topologie qui configurent les bases de données ou de créer manuellement les bases de données avec des cmdlets Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14019-108">Additionally, each SQL Server instance must be installed and available prior to completing the steps in Topology Builder that set up the databases, or manually creating the databases with Windows PowerShell cmdlets.</span></span> <span data-ttu-id="14019-109">Pour plus d’informations sur la prise en charge de SQL Server, voir [Configuration matérielle pour Lync Server 2013](lync-server-2013-hardware-setup.md).</span><span class="sxs-lookup"><span data-stu-id="14019-109">For details about SQL Server supportability, see [Hardware setup for Lync Server 2013](lync-server-2013-hardware-setup.md).</span></span>

<div>

## <a name="to-install-microsoft-sql-server-2012"></a><span data-ttu-id="14019-110">Pour installer Microsoft SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="14019-110">To install Microsoft SQL Server 2012</span></span>

  - <span data-ttu-id="14019-111">Pour plus d’informations, consultez la documentation Microsoft SQL Server 2012 à l’adresse suivante : <https://technet.microsoft.com/library/bb500395(v=sql.110).aspx> .</span><span class="sxs-lookup"><span data-stu-id="14019-111">See the Microsoft SQL Server 2012 documentation at: <https://technet.microsoft.com/library/bb500395(v=sql.110).aspx>.</span></span>

<span data-ttu-id="14019-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14019-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

