---
title: 'Lync Server 2013 : exigences techniques de l’archivage'
description: 'Lync Server 2013 : exigences techniques d’archivage.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Archiving
ms:assetid: 896d60e2-be4b-462d-8357-4cd307ab7304
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205059(v=OCS.15)
ms:contentKeyID: 48184732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6100753ad2c62424eb68c8c258094ba51848170e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423385"
---
# <a name="technical-requirements-for-archiving-in-lync-server-2013"></a><span data-ttu-id="32fd1-103">Configuration technique requise pour l’archivage dans Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32fd1-103">Technical requirements for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32fd1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32fd1-104">

<span> </span></span></span>

<span data-ttu-id="32fd1-105">_**Dernière modification de la rubrique :** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="32fd1-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="32fd1-106">Les exigences techniques de Lync Server 2013 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32fd1-106">Lync Server 2013 technical requirements include the following:</span></span>

  - <span data-ttu-id="32fd1-107">Exigences d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="32fd1-107">Infrastructure requirements.</span></span>

  - <span data-ttu-id="32fd1-108">Logiciels requis qui doivent être installés pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-108">Prerequisite software that must be installed for Archiving.</span></span>

  - <span data-ttu-id="32fd1-109">Exigences en matière de stockage des données pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-109">Data storage requirements for Archiving.</span></span>

  - <span data-ttu-id="32fd1-110">Exigences relatives à l’échelle et considérations relatives à votre déploiement d’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-110">Scaling requirements and considerations for your Archiving deployment.</span></span>

  - <span data-ttu-id="32fd1-111">Exigences et considérations en matière de performances pour vos bases de données d’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-111">Performance requirements and considerations for your Archiving databases.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="32fd1-112">Les informations de mise à l’échelle et de performance ne sont pas disponibles dans la version 2013 de Lync Server.</span><span class="sxs-lookup"><span data-stu-id="32fd1-112">Scaling and performance information is not available in this Lync Server 2013 release.</span></span>



</div>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="32fd1-113">Exigences d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="32fd1-113">Infrastructure Requirements</span></span>

<span data-ttu-id="32fd1-114">Les exigences d’infrastructure d’archivage de Lync Server 2013 sont les mêmes que pour le déploiement de Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32fd1-114">Lync Server 2013 Archiving infrastructure requirements are the same as for deployment of Lync Server 2013.</span></span> <span data-ttu-id="32fd1-115">Pour plus d’informations, reportez-vous à la rubrique [détermination de votre configuration d’infrastructure requise pour Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) dans la documentation de planification.</span><span class="sxs-lookup"><span data-stu-id="32fd1-115">For details, see [Determining your infrastructure requirements for Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-prerequisites"></a><span data-ttu-id="32fd1-116">Archivage requis</span><span class="sxs-lookup"><span data-stu-id="32fd1-116">Archiving Prerequisites</span></span>

<span data-ttu-id="32fd1-117">Lync Server 2013 simplifie les conditions préalables à l’archivage pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="32fd1-117">Lync Server 2013 streamlines prerequisites for Archiving because of the following:</span></span>

  - <span data-ttu-id="32fd1-118">Le serveur d’archivage n’est plus un rôle serveur.</span><span class="sxs-lookup"><span data-stu-id="32fd1-118">Archiving Server is no longer a server role.</span></span> <span data-ttu-id="32fd1-119">Au lieu de cela, les agents de collection de données unifiés s’exécutent sur les serveurs frontaux d’un pool et de serveurs Standard Edition pour capturer les données pour l’archivage, de sorte que vous ne configurez pas des plateformes système distinctes pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-119">Instead, Unified Data Collection Agents run on the Front End Servers in a pool and Standard Edition servers to capture data for Archiving, so you do not set up separate system platforms for Archiving.</span></span>

  - <span data-ttu-id="32fd1-120">L’archivage utilise le stockage de fichiers de Lync Server 2013 pour stocker temporairement les fichiers de contenu de la réunion, de sorte que vous n’avez pas configuré de magasin de fichiers distinct pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-120">Archiving uses the Lync Server 2013 file storage for temporary storage of meeting content files, so you do not set up a separate file store for archiving.</span></span>

  - <span data-ttu-id="32fd1-121">Dans Lync Server 2013, Message Queuing n’est pas requis.</span><span class="sxs-lookup"><span data-stu-id="32fd1-121">In Lync Server 2013, Message Queuing is not required.</span></span>

</div>

<div>

## <a name="data-storage-requirements-for-archiving"></a><span data-ttu-id="32fd1-122">Exigences en matière de stockage des données pour l’archivage</span><span class="sxs-lookup"><span data-stu-id="32fd1-122">Data Storage Requirements for Archiving</span></span>

<span data-ttu-id="32fd1-123">Par ailleurs, vous devez configurer l’infrastructure pour le stockage d’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-123">Additionally, you need to set up the infrastructure for Archiving storage.</span></span> <span data-ttu-id="32fd1-124">Cela comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="32fd1-124">This includes one or both of the following:</span></span>

  - <span data-ttu-id="32fd1-125">**Stockage Microsoft Exchange**.</span><span class="sxs-lookup"><span data-stu-id="32fd1-125">**Microsoft Exchange storage**.</span></span> <span data-ttu-id="32fd1-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span><span class="sxs-lookup"><span data-stu-id="32fd1-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span></span> <span data-ttu-id="32fd1-127">Si vous souhaitez utiliser l’intégration de Microsoft Exchange de sorte que les données d’archive Lync soient stockées avec les données de conformité Exchange, vous devez utiliser Exchange 2013 pour votre déploiement Exchange et garantir que la taille de stockage maximale prend en charge le stockage des fichiers de contenu de la réunion.</span><span class="sxs-lookup"><span data-stu-id="32fd1-127">If you want to use Microsoft Exchange integration so that Lync archive data is stored with Exchange compliance data, you must use Exchange 2013 for your Exchange deployment and ensure that the maximum storage size supports storage of the meeting content files.</span></span> <span data-ttu-id="32fd1-128">Si vous déployez l’archivage à l’aide de l’option d’intégration de Microsoft Exchange, les données d’archive Lync sont stockées avec les données de conformité Exchange 2013 uniquement pour les utilisateurs qui sont hébergés sur vos serveurs Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="32fd1-128">If you deploy Archiving using the Microsoft Exchange integration option, Lync archive data is stored with Exchange 2013 compliance data only for the users who are homed on your Exchange 2013 servers.</span></span> <span data-ttu-id="32fd1-129">Vous devez déployer Exchange 2013 avant de déployer et d’activer l’archivage à l’aide de l’option d’intégration de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="32fd1-129">You must deploy Exchange 2013 prior to deploying and enabling Archiving using the Microsoft Exchange integration option.</span></span> <span data-ttu-id="32fd1-130">Si vous choisissez d’utiliser le stockage Exchange 2013, vous n’avez pas besoin de déployer des bases de données SQL Server distinctes pour l’archivage, sauf si vous avez des utilisateurs de Lync qui ne sont pas hébergés sur vos serveurs Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="32fd1-130">If you choose to use Exchange 2013 storage, you do not need to deploy separate SQL Server databases for Archiving, unless you have Lync users who are not homed on your Exchange 2013 servers.</span></span>

  - <span data-ttu-id="32fd1-131">**Stockage de base de données SQL Server pour l’archivage**.</span><span class="sxs-lookup"><span data-stu-id="32fd1-131">**SQL Server database storage for Archiving**.</span></span> <span data-ttu-id="32fd1-132">Pour prendre en charge les utilisateurs qui ne sont pas hébergés sur des serveurs Exchange 2013 ou si vous ne voulez pas utiliser l’option d’intégration de Microsoft Exchange, vous devez déployer le stockage d’archivage à l’aide d’une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="32fd1-132">To support users who are not homed on Exchange 2013 servers, or if you do not want to use the Microsoft Exchange integration option, you must deploy Archiving storage using a SQL Server database.</span></span> <span data-ttu-id="32fd1-133">Lync Server 2013 prend en charge les versions 64 bits suivantes de SQL Server :</span><span class="sxs-lookup"><span data-stu-id="32fd1-133">Lync Server 2013 supports the following 64-bit versions of SQL Server:</span></span>
    
      - <span data-ttu-id="32fd1-134">Microsoft SQL Server 2008 R2 entreprise</span><span class="sxs-lookup"><span data-stu-id="32fd1-134">Microsoft SQL Server 2008 R2 Enterprise</span></span>
    
      - <span data-ttu-id="32fd1-135">Microsoft SQL Server 2008 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="32fd1-135">Microsoft SQL Server 2008 R2 Standard</span></span>
    
      - <span data-ttu-id="32fd1-136">Microsoft SQL Server 2012 entreprise</span><span class="sxs-lookup"><span data-stu-id="32fd1-136">Microsoft SQL Server 2012 Enterprise</span></span>
    
      - <span data-ttu-id="32fd1-137">Microsoft SQL Server 2012 standard</span><span class="sxs-lookup"><span data-stu-id="32fd1-137">Microsoft SQL Server 2012 Standard</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="32fd1-138">Microsoft SQL Server 2008 R2 Express et Microsoft SQL Server 2012 Express ne sont pas pris en charge pour l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-138">Microsoft SQL Server 2008 R2 Express and Microsoft SQL Server 2012 Express are not supported for Archiving.</span></span> <span data-ttu-id="32fd1-139">les versions 32 bits de SQL Server ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="32fd1-139">32-bit versions of SQL Server are not supported.</span></span> <span data-ttu-id="32fd1-140">Pour plus d’informations et de restrictions concernant SQL Server, voir <A href="lync-server-2013-database-software-support.md">prise en charge de logiciels de base de données dans Lync Server 2013</A> dans la documentation de planification ou dans la documentation sur la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="32fd1-140">For additional SQL Server requirements and restrictions, see <A href="lync-server-2013-database-software-support.md">Database software support in Lync Server 2013</A> in the Planning documentation or in the Supportability documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="32fd1-141">Vous devez configurer les plates-formes SQL Server avant de déployer et d’activer l’archivage.</span><span class="sxs-lookup"><span data-stu-id="32fd1-141">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="32fd1-142">Si le compte à utiliser pour la publication de la topologie est doté des droits et autorisations d’administrateur appropriés, vous pouvez créer la base de données d’archivage (LcsLog) lorsque vous publiez votre topologie.</span><span class="sxs-lookup"><span data-stu-id="32fd1-142">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="32fd1-143">Vous pouvez également créer la base de données ultérieurement, y compris dans le cadre de la procédure d’installation.</span><span class="sxs-lookup"><span data-stu-id="32fd1-143">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="32fd1-144">Pour plus d’informations sur SQL Server, voir le site TechCenter SQL Server à l’adresse [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .</span><span class="sxs-lookup"><span data-stu-id="32fd1-144">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<span data-ttu-id="32fd1-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32fd1-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

