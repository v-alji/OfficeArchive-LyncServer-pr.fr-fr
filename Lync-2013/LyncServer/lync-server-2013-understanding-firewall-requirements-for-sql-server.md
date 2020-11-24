---
title: 'Lync Server 2013 : Description des exigences de pare-feu pour SQL Server'
description: 'Lync Server 2013 : présentation de la configuration requise pour le pare-feu pour SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394849"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="f6d45-103">Description des exigences de pare-feu pour SQL Server avec Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6d45-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6d45-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6d45-104">

<span> </span></span></span>

<span data-ttu-id="f6d45-105">_**Dernière modification de la rubrique :** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f6d45-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f6d45-106">Dans le cadre d’un déploiement Standard Edition, des exceptions de pare-feu sont créées automatiquement lors de la configuration de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f6d45-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="f6d45-107">Toutefois, pour les déploiements Enterprise Edition, vous devez configurer les exceptions de pare-feu manuellement sur le serveur principal SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f6d45-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="f6d45-108">Le protocole TCP/IP permet d’utiliser un port donné une seule fois pour une adresse IP donnée.</span><span class="sxs-lookup"><span data-stu-id="f6d45-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="f6d45-109">En d’autres termes, pour le serveur SQL Server, vous pouvez affecter l’instance de base de données par défaut, le port TCP 1433.</span><span class="sxs-lookup"><span data-stu-id="f6d45-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="f6d45-110">Pour tous les autres cas, vous devez utiliser le gestionnaire de configuration SQL Server pour attribuer des ports uniques et inutilisés.</span><span class="sxs-lookup"><span data-stu-id="f6d45-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="f6d45-111">Cette rubrique aborde les thèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="f6d45-111">This topic covers:</span></span>

  - <span data-ttu-id="f6d45-112">Configuration requise pour une exception de pare-feu lors de l’utilisation de l’instance par défaut</span><span class="sxs-lookup"><span data-stu-id="f6d45-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="f6d45-113">Configuration requise pour une exception de pare-feu pour le service SQL Server Browser</span><span class="sxs-lookup"><span data-stu-id="f6d45-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="f6d45-114">Configuration requise pour les ports d’écoute statique lors de l’utilisation d’instances nommées</span><span class="sxs-lookup"><span data-stu-id="f6d45-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="f6d45-115">Configuration requise pour une exception de pare-feu lors de l’utilisation de l’instance par défaut</span><span class="sxs-lookup"><span data-stu-id="f6d45-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="f6d45-116">Si vous utilisez l’instance par défaut de SQL Server pour une base de données lors du déploiement de Lync Server 2013, les exigences de règle de pare-feu suivantes permettent de garantir la communication du pool frontal à l’instance SQL Server par défaut.</span><span class="sxs-lookup"><span data-stu-id="f6d45-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6d45-117">Protocole</span><span class="sxs-lookup"><span data-stu-id="f6d45-117">Protocol</span></span></th>
<th><span data-ttu-id="f6d45-118">Port</span><span class="sxs-lookup"><span data-stu-id="f6d45-118">Port</span></span></th>
<th><span data-ttu-id="f6d45-119">Direction</span><span class="sxs-lookup"><span data-stu-id="f6d45-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6d45-120">TCP</span><span class="sxs-lookup"><span data-stu-id="f6d45-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="f6d45-121">1433</span><span class="sxs-lookup"><span data-stu-id="f6d45-121">1433</span></span></p></td>
<td><p><span data-ttu-id="f6d45-122">Entrant sur SQL Server</span><span class="sxs-lookup"><span data-stu-id="f6d45-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="f6d45-123">Configuration requise pour une exception de pare-feu pour le service SQL Server Browser</span><span class="sxs-lookup"><span data-stu-id="f6d45-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="f6d45-124">Le service de navigateur SQL Server détermine les instances de base de données et communique le port que l’instance (nommée ou par défaut) est configurée pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f6d45-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6d45-125">Protocole</span><span class="sxs-lookup"><span data-stu-id="f6d45-125">Protocol</span></span></th>
<th><span data-ttu-id="f6d45-126">Port</span><span class="sxs-lookup"><span data-stu-id="f6d45-126">Port</span></span></th>
<th><span data-ttu-id="f6d45-127">Direction</span><span class="sxs-lookup"><span data-stu-id="f6d45-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6d45-128">UDP</span><span class="sxs-lookup"><span data-stu-id="f6d45-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="f6d45-129">1434</span><span class="sxs-lookup"><span data-stu-id="f6d45-129">1434</span></span></p></td>
<td><p><span data-ttu-id="f6d45-130">Entrant</span><span class="sxs-lookup"><span data-stu-id="f6d45-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="f6d45-131">Configuration requise pour les ports d’écoute statique lors de l’utilisation d’instances nommées</span><span class="sxs-lookup"><span data-stu-id="f6d45-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="f6d45-132">Lors de l’utilisation d’instances nommées dans la configuration SQL Server pour les bases de données prenant en charge Lync Server 2013, vous devez configurer les ports statiques à l’aide du gestionnaire de configuration SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f6d45-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="f6d45-133">Une fois que les ports statiques ont été attribués à chaque instance nommée, vous créez des exceptions pour chaque port statique dans le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="f6d45-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6d45-134">Protocole</span><span class="sxs-lookup"><span data-stu-id="f6d45-134">Protocol</span></span></th>
<th><span data-ttu-id="f6d45-135">Port</span><span class="sxs-lookup"><span data-stu-id="f6d45-135">Port</span></span></th>
<th><span data-ttu-id="f6d45-136">Direction</span><span class="sxs-lookup"><span data-stu-id="f6d45-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6d45-137">TCP</span><span class="sxs-lookup"><span data-stu-id="f6d45-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="f6d45-138">Défini de manière statique</span><span class="sxs-lookup"><span data-stu-id="f6d45-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="f6d45-139">Entrant</span><span class="sxs-lookup"><span data-stu-id="f6d45-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="f6d45-140">Documentation SQL Server</span><span class="sxs-lookup"><span data-stu-id="f6d45-140">SQL Server Documentation</span></span>

<span data-ttu-id="f6d45-141">La documentation Microsoft SQL Server 2012 fournit des instructions détaillées sur la configuration de l’accès par le pare-feu aux bases de données.</span><span class="sxs-lookup"><span data-stu-id="f6d45-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="f6d45-142">Pour plus d’informations sur Microsoft SQL Server 2012, voir « Configuration du pare-feu Windows pour autoriser l’accès à SQL Server » à l’adresse [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) .</span><span class="sxs-lookup"><span data-stu-id="f6d45-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="f6d45-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6d45-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

