---
title: 'Lync Server 2013 : Autorisations de déploiement de SQL Server'
description: 'Lync Server 2013 : autorisations de déploiement pour SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment permissions for SQL Server
ms:assetid: 56ea0c02-bcf5-4d45-aa13-570531c29074
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398375(v=OCS.15)
ms:contentKeyID: 48184197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be5985bc8f3173b03d8969d3dd58cfbf8daf85f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394928"
---
# <a name="deployment-permissions-for-sql-server-in-lync-server-2013"></a><span data-ttu-id="0db8c-103">Autorisations de déploiement de SQL Server dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0db8c-103">Deployment permissions for SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0db8c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0db8c-104">

<span> </span></span></span>

<span data-ttu-id="0db8c-105">_**Dernière modification de la rubrique :** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="0db8c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="0db8c-106">Microsoft SQL Server 2012 a des exigences spécifiques lors de l’installation et du déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0db8c-106">Microsoft SQL Server 2012 has specific requirements when installing and deploying Lync Server 2013.</span></span> <span data-ttu-id="0db8c-107">Dans la mesure où Windows et SQL Server définissent la sécurité d’une manière différente, la connexion en tant qu’administrateur dans le domaine Active Directory n’accorde pas implicitement des autorisations pour SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-107">Because Windows and SQL Server define their security differently, logging in as an administrator in the Active Directory domain does not implicitly grant permissions for SQL Server.</span></span> <span data-ttu-id="0db8c-108">Vous devez également être membre de l’entité sysadmin sur le serveur SQL Server que vous configurez.</span><span class="sxs-lookup"><span data-stu-id="0db8c-108">You must also be a member of the sysadmin entity on the SQL Server-based server you are configuring.</span></span>

<div>

## <a name="permissions-required-for-database-and-lync-server-installation"></a><span data-ttu-id="0db8c-109">Autorisations requises pour l’installation de base de données et de Lync Server</span><span class="sxs-lookup"><span data-stu-id="0db8c-109">Permissions Required for Database and Lync Server Installation</span></span>

<span data-ttu-id="0db8c-110">Les options suivantes décrivent trois autorisations et des associations d’appartenance de groupe pour l’installation de fichiers Lync Server 2013 et de bases de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-110">The following options detail three permissions and group membership associations for installation of Lync Server 2013 files and SQL Server databases.</span></span> <span data-ttu-id="0db8c-111">Choisissez le scénario qui correspond le mieux aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0db8c-111">Choose the scenario that best meets the requirements of your organization.</span></span>

### <a name="permissions-and-group-membership-associations"></a><span data-ttu-id="0db8c-112">Autorisations et associations d’appartenance aux groupes</span><span class="sxs-lookup"><span data-stu-id="0db8c-112">Permissions and Group Membership Associations</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0db8c-113">Rôle SQL Server ou Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0db8c-113">SQL Server or Lync Server 2013 role</span></span></th>
<th><span data-ttu-id="0db8c-114">Role-Typical les autorisations et l’appartenance aux groupes SQL Server</span><span class="sxs-lookup"><span data-stu-id="0db8c-114">Role-Typical SQL Server permissions and group membership</span></span></th>
<th><span data-ttu-id="0db8c-115">Rôles : autorisations et appartenances aux groupes Lync Server 2013 typiques</span><span class="sxs-lookup"><span data-stu-id="0db8c-115">Role-typical Lync Server 2013 permissions and group membership</span></span></th>
<th><span data-ttu-id="0db8c-116">Résultat des autorisations</span><span class="sxs-lookup"><span data-stu-id="0db8c-116">Permissions outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0db8c-117">Administrateur Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0db8c-117">Lync Server 2013 administrator</span></span></p></td>
<td><p><span data-ttu-id="0db8c-118">Doit être membre du groupe de sécurité SQL Server sysadmin et membre du groupe administrateurs SQL Server local.</span><span class="sxs-lookup"><span data-stu-id="0db8c-118">Must be granted membership of sysadmins SQL Server security group and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="0db8c-119">Doit être membre du groupe RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0db8c-119">Must be a member of the RTCUniversalServerAdmins group</span></span></p></td>
<td><p><span data-ttu-id="0db8c-120">L’administrateur de Lync Server 2013 dispose des autorisations nécessaires pour installer les bases de données Lync Server 2013 et SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-120">Lync Server 2013 administrator has the proper permissions to install both Lync Server 2013 and SQL Server databases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0db8c-121">Administrateur SQL Server</span><span class="sxs-lookup"><span data-stu-id="0db8c-121">SQL Server administrator</span></span></p></td>
<td><p><span data-ttu-id="0db8c-122">Membre du groupe SQL Server sysadmin (ou équivalent) et membre du groupe administrateurs locaux SQL Server</span><span class="sxs-lookup"><span data-stu-id="0db8c-122">SQL Server sysadmin group member (or equivalent) and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="0db8c-123">Doit être membre du groupe RTCUniversalServerReadOnly</span><span class="sxs-lookup"><span data-stu-id="0db8c-123">Must be a member of the RTCUniversalServerReadOnly group</span></span></p></td>
<td><p><span data-ttu-id="0db8c-124">L’administrateur SQL Server dispose des autorisations appropriées pour installer à la fois Lync Server 2013 et les bases de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-124">SQL Server administrator has the proper permissions to install both Lync Server 2013 and SQL Server databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0db8c-125">Les administrateurs partagent les tâches d’installation</span><span class="sxs-lookup"><span data-stu-id="0db8c-125">Both administrators sharing installation duties</span></span></p></td>
<td><p><span data-ttu-id="0db8c-126">L’administrateur SQL Server est membre du groupe sysadmins (ou équivalent) et membre du groupe administrateurs SQL Server local.</span><span class="sxs-lookup"><span data-stu-id="0db8c-126">SQL Server administrator is member of sysadmins group (or equivalent) and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="0db8c-127">L’administrateur Lync Server 2013 est membre de RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0db8c-127">Lync Server 2013 administrator is member of RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="0db8c-128">L’administrateur 2013 de Lync Server peut installer Lync Server 2013, mais ne peut pas installer les bases de données.</span><span class="sxs-lookup"><span data-stu-id="0db8c-128">The Lync Server 2013 administrator can install Lync Server 2013, but cannot install the databases.</span></span> <span data-ttu-id="0db8c-129">L’administrateur SQL Server a recours aux cmdlets Lync Server Management Shell et Windows PowerShell fournies par l’administrateur 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-129">The SQL Server administrator uses the Lync Server Management Shell and Windows PowerShell cmdlets provided by the Lync Server 2013 administrator to install the databases.</span></span> <span data-ttu-id="0db8c-130">Lync Server 2013 Management Shell utilisé par l’administrateur SQL Server est installé sur le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="0db8c-130">The Lync Server 2013 Management Shell used by the SQL Server administrator is installed on the Front End Server.</span></span> <span data-ttu-id="0db8c-131">Cela évite d’avoir à installer les outils d’administration de Lync Server 2013 sur le serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0db8c-131">This eliminates the need to install the Lync Server 2013 administrative tools on the SQL Server-based server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0db8c-132">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0db8c-132">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

